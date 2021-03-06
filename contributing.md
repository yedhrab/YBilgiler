---
description: Projeye katkı sağlamak isteyenler için bilgilendirme
---

# 💖 Katkıda Bulunma Rehberi

## 💡 İçerik Desteğinde Bulunma veya Fikir Belirtme

* ✨ Verimli olabilecek yapı tekliflerine ve **yapıcı** eleştirilere açığım
* 💡 Tavsiyelerin veya hata tespitlerin varsa [🦋 Issue](https://github.com/yedhrab/YWiki/issues) açabilirsin
* **🏗️ Yapıcı** eleştirileriniz veya fikirleriniz varsa sağ üst köşedeki  **🏹 Edit on GitHub** alanından fikirlerinizi belirtebilirsiniz

{% page-ref page="programlama/yardimci/markdown/" %}

{% hint style="warning" %}
**📢** [**Markdown**](programlama/yardimci/markdown/)**'a uygun şekilde katkıda bulunursanız hoş olur 😊**
{% endhint %}

## 👷‍ Sayfaların Tasarımı ve Notların Tutulma Yapısı

```text
- Genel veya Sektörel Başlık
  - Bilgi verilecek konu veya platform ismi
    - Alt başlık
      - Bilgi 1
      - Bilgi 2
      - Bilgi 3
    - Alt başlık 2
      - ...
    - ...
  - ...
- ...
...
```

## 📑 İçerik Yazma Formatı

* 🚀 Başlık ile alakalı bir emoji koyman verimlilik adına çok etkilidir.
* 🎇 Windows üzerinde, ❖ Win Ş ile emoji klavyesini açabilirsin
* 🐧 Linux için [😎 Emoji Selector](https://extensions.gnome.org/extension/1162/emoji-selector/) eklentisini kullanabilirsin

```text
## 🌟 Başlık

Giriş cümlesi veya alakalı cümle.

- Alaklı maddesel bilgiler
- Bilgi 2

> Varsa ek yorum

<!-- Tablo oluşturman gerekiyorsa -->
| Tablo        | Tablo1                      |
| ------------ | --------------------------- |
| `<değişken>` | Tablosal yapı ile örnekleme |

- `<değişken>` Tablo değişkenlerini açıklama
  - Örn: `kod` örneklendirme


<!-- Tek bağlantı varsa -->
> [Kaynak ismi](https://yemreak.com)

<!-- Birden fazla bağlantı varsa -->
> Ek bağlantılar:
>
> - [Link](https://yemreak.com)
> - [Link](https://yemreak.com)
> - [Link](https://yemreak.com)
```

## ✍ Çalışma Notları

* 👀 Markdown hakkında detaylı açıklamalara [📑 Markdown](https://wiki.yemreak.com/programlama-notlari/yardimci-diller/markdown) bağlantısından erişebilirsin
* ✨ Her şey **dinamik** olmalı
* 💖 Önemli notlar ve başlıklar **bold**
* 🎛️ Butonlar ve tıklanabilir öğeler button `<kbd>button</kbd>`
* 🚅 Terimler _italik_ `_italik_`
  * 👨‍💼 Önce normal yaz, sonrasında ✲ Ctrl + H ile metinleri italik hale dönüştür
* 🧱 Kalıplar ve sabit ifadeler \` arasına yazılmalı
* 👨‍💻 Kodlar \`\`\` arasına yazılmalı
* 🧮 Matematikler \(latex\) $latex$ `$$latex$$ (gitbook) veya $latex$ (github)`

{% page-ref page="programlama/yardimci/markdown/" %}

## 🏃‍ Online Ortamda Projeye Hızlıca Katkıda Bulunma

GitHub projelerini `clone` yapıp, internet kotanı harcamak yerine, web üzerinden katkıda bulunabilirsin.

* 👮‍♂️ Katkı sağlama işlemi GitHub hesabı gerektirir.
* ✨ Güncel bilgiler için [🌍 GitHub Web](proje-yonetimi/github/web.md) yazıma bakabilirsin

{% page-ref page="proje-yonetimi/github/web.md" %}

## 👨‍💻 Geliştirici Notları

### 📃 Alt Sayfa Bağlantılarının Güncellenmesi

Güncelleme işlemleri için gereksinimler

* `pip install ypackage` ile `ypackage` kurulumu
* `.ysubmodules` dosyası
* `ygitbookintegration . -u` komutu

