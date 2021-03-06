---
description: Her değişikliği belirten commitler hakkında detaylar
---

# ✨ Git Commit İşlemleri

## ‍🧙‍♂ Hata Mesajsız Commit

* ❣️ Entegrasyon araçları için hata mesajları önemlidir
* 💁‍♂️ İşlem tamamlanmadığıda hata mesajı gelmesini engellemek için alttaki yapıyı kullan
* 💫 GitHub workflows vb yerlerde işlemlerin etmesini sağlar

```bash
echo `git add -A && git commit -m "Added license headers"`
```

{% hint style="info" %}
‍🧙‍♂ Detaylı bilgi için [How to let Jenkins git commit only if there are changes?](https://stackoverflow.com/questions/22040113/how-to-let-jenkins-git-commit-only-if-there-are-changes) alanına bakabilirsin.
{% endhint %}

## 🧼 Son Commit'i Kaldırma

```bash
git reset --soft HEAD~1  # 1 tane commiti kaldırır, stage olarak korur
git reset --hard HEAD~1  # 1 tane commiti tamamen siler
git push origin +master --force # zorla karşıyı güncelleme
```

{% hint style="info" %}
‍🧙‍♂ Detaylı bilgi için [How can I remove commit on GitHub](https://stackoverflow.com/a/448929/9770490) alanına bakabilirsin.
{% endhint %}

## 🔄 Local Değişiklikleri Remote ile Güncelleme

```bash
git reset --hard origin/master
```

## 💦 Dosyayı Git Geçmişinden Kaldırma

```bash
git rm --cached <file_path>
git commit --amend -CHEAD
git push --force
```

{% hint style="info" %}
‍🧙‍♂ Detaylı bilgi için [Removing files from a repository's history](https://docs.github.com/en/github/managing-large-files/removing-files-from-a-repositorys-history) alanına bakabilirsin.
{% endhint %}

## Son Değişiklikleri Geri Alma

```bash
git revert --strategy resolve <commit>
```

> [https://stackoverflow.com/a/3207170](https://stackoverflow.com/a/3207170)

## Pull From işlemini Geri Alma

Bunun için başka bir branch'a geçip, geri almak istediğimiz branch'ı siliyoruz.

```bash
git checkout <branch2>
git branch -D <branch1>
git checkout <branch1>
```

* `<branch1>` Düzeltilmek istenen branch
* `<branch2>` Farkı herhangi bir branch

## Tüm Commitlerden Dizini Kaldırma

Alttaki script'te `<dizin>` yazan kısmı kaldırmak istediğiniz dizinin ismi ile değiştirin.

```bash
git filter-branch --tree-filter "rm -rf <dizin>" --prune-empty -f HEAD
git for-each-ref --format="%(refname)" refs/original/ | xargs -n 1 git update-ref -d
echo <dizin>/ >> .gitignore
git add .gitignore
git commit -m 'Removing sessions from git history'
git gc
git push origin master --force
```

## Git Tag'ları Kaldırma \(Release Aşamasındakiler\)

```bash
# Localde kaldırma
git tag -d `git tag | grep -E '.'`

# Remote'da kaldırma
git ls-remote --tags origin | awk '/^(.*)(s+)(.*[a-zA-Z0-9])$/ {print ":" $2}' | xargs git push origin
```

> [Deleting Git Tags Locally and on Github](https://www.alwaystwisted.com/articles/deleting-git-tags-locally-and-on-github)

