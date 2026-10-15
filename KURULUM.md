# Günce'yi telefona uygulama olarak kurma

Bu klasör, Günce'nin telefona eklenen uygulama sürümüdür. Ana ekranda kendi simgesiyle durur, tam ekran açılır, internet olmadan da çalışır.

## Klasörde ne var?

| Dosya | Ne işe yarar |
|---|---|
| `index.html` | Uygulamanın kendisi |
| `manifest.webmanifest` | Uygulama adı, simgesi, renkleri (telefon bunu okuyup "uygulama" olarak kurar) |
| `sw.js` | İnternetsiz çalışmayı ve bildirimleri sağlar |
| `icons/` | Ana ekran simgeleri |

## 1. Bir kez internete koy (ücretsiz, ~5 dakika)

Telefonun bunu uygulama olarak kurabilmesi için dosyaların **https** ile açılan bir adreste durması gerekir. En kolayı GitHub Pages:

1. github.com'da oturum aç → sağ üstte **+** → **New repository**.
2. Ad: `gunce` · **Public** seç → **Create repository**.
3. Açılan sayfada **uploading an existing file** bağlantısına tıkla.
4. Zip'ten çıkan dosyaların **hepsini** (`icons` klasörü dahil) sürükleyip bırak → **Commit changes**.
5. Repo'da **Settings → Pages** → *Branch* olarak `main` ve `/ (root)` seç → **Save**.
6. 1–2 dakika sonra adresin hazır: `https://KULLANICI-ADIN.github.io/gunce/`

> Öğrenci olduğun için GitHub Student Developer Pack ile repo'yu **Private** da yapabilirsin. Kayıtların zaten repo'da değil, telefonda durur; repo'da sadece uygulamanın kodu var (profil adları dahil).

Alternatif: app.netlify.com/drop adresine klasörü sürükle bırak, ücretsiz hesapla adresi kalıcı yap.

## 2. Telefona ekle

**Android (Chrome):** adresi aç → çıkan **Uygulamayı yükle** düğmesine dokun. Çıkmazsa sağ üstte **⋮ → Uygulamayı yükle / Ana ekrana ekle**.

**iPhone (Safari):** adresi aç → alttaki **Paylaş** düğmesi → **Ana Ekrana Ekle** → **Ekle**.

Artık ana ekranda kırmızı-beyaz takvim yaprağı simgeli **Günce** var.

## 3. Reyhan için

Reyhan kendi telefonunda aynı adresi açıp aynı şekilde eklesin, girişte **Reyhan**'ı seçsin.

- Her telefon kendi kayıtlarını **sadece kendi içinde** tutar; hiçbir sunucuya gitmez.
- Yani Reyhan'ın döngü kayıtları yalnızca onun telefonunda durur, senin bile erişimin olmaz.
- İsterse Ayarlar'dan 4 haneli PIN koyabilir.

## 4. Mevcut kayıtlarını taşı (isteğe bağlı)

1. Claude'daki Günce sayfasını aç → **Ayarlar → Yedeği indir**.
2. Telefondaki uygulamada **Ayarlar → Yedekten geri yükle** → indirdiğin dosyayı seç.

Kayıtlar hangi profil açıksa ona yüklenir.

## 5. Bilmen gerekenler

- **Yedek al.** Uygulamayı silersen ya da tarayıcı verilerini temizlersen kayıtlar da gider. Ayarlar → **Yedeği indir** ile arada bir yedek al (iPhone'da "Dosyalar'a kaydet", Android'de Drive seçebilirsin). Sayfanın altında "son yedek" tarihi yazar.
- **Senkron yok.** Telefon ve bilgisayar ayrı kayıt tutar. Senkron istersen Claude'daki sürümü kullanmaya devam et.
- **Bildirimler.** Ayarlar → **Bildirimlere izin ver**. Uygulama açıkken saati gelen hatırlatmalar telefon bildirimi olarak gelir. Uygulama tamamen kapalıyken bildirim gönderilemez.
- **Güncelleme.** Yeni sürüm gelirse dosyaları repo'da değiştirmen yeterli; uygulama bir sonraki açılışta kendini yeniler.
