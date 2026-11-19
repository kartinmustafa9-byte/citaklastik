# Çıtak Oto Lastik — Proje Notları

Son güncelleme: 19 Kasım 2026

## Özet
- **İşletme:** Çıtak Oto Lastik. Lastik tamiri, lastik satışı (yeni ve 2. el), lastik değişimi ve yol yardım hizmeti veriyor.
- **Adres:** Andiçen Mah. Gönlübol Cd. No:2, Sincan/Ankara
- **Telefon / WhatsApp:** 0536 332 4634
- **Canlı site:** https://citak-oto-lastik.vercel.app (eski adres https://citaklastik.vercel.app da çalışıyor)
- **Yönetim paneli:** `/admin` → `#yonetim`. Şifre koda yazılmıyor, yalnızca karması (hash) tutuluyor.
- **Yayın düzeni:** GitHub `kartinmustafa9-byte/citaklastik` (main dalı) → Vercel. Her push otomatik yayına alınıyor, yaklaşık 40 saniye sürüyor.

## Sabit kurallar
- Sitede hiçbir yerde fiyat yazmaz. Müşteri fiyat için arar ya da WhatsApp'tan yazar.
- Mevcut yapı ve tasarım bozulmaz. Yalnızca bozuk olan yer düzeltilir.
- Şirket yok, şahıs işletmesi. KVKK ve yasal sayfa buna göre hazırlandı.
- Uygulama yok, yalnızca web sitesi var. "Ana ekrana ekle" iOS'ta ve Android'de çalışır.

## Dosyalar
| Dosya | Görevi |
|---|---|
| `index.html` | Tek dosyalık site. Sinematik 3D sahne gömülü, Three.js ayrı yüklenmiyor. |
| `admin/index.html` | `#yonetim` sayfasına yönlendirir |
| `manifest.webmanifest` | Ana ekran adı "Çıtak Oto Lastik", simgeler, kısayollar |
| `icon-v2-180/192/512.png`, `icon-v2-maskable-512.png` | Lastik ve sarı "Ç" logosu |
| `sw.js` | Önbellek (`citak-v2`) |
| `vercel.json` | cleanUrls ve güvenlik başlıkları |
| `robots.txt`, `sitemap.xml` | Google için |

## Yapılanlar (sırasıyla)
1. Site GitHub ve Vercel üzerinden yayına alındı. Vercel giriş koruması kapatıldı, site herkese açık.
2. Adres `citak-oto-lastik.vercel.app` olarak ayarlandı.
3. Sarı kayan şerit: döngü kesintisiz hale getirildi, titreme giderildi (GPU animasyonu, 110 saniyede bir tur).
4. Ana ekran adı kısaltıldı: "Çıtak Oto Lastik". Yeni logo yapıldı.
5. iOS'ta eski "Ç" simgesi çıkıyordu. Sebebi simge etiketlerinin `<body>` içinde kalmasıydı, `<head>` içine taşındı.
6. Yerel SEO eklendi. Başlık ve açıklamada Sincan/Ankara, lastik tamiri ve yol yardım geçiyor. Yapılandırılmış veri olarak TireShop eklendi. canonical, robots ve sitemap eklendi.
7. Adres eklendi: harita kartında, iletişim sayfasında, yapılandırılmış veride ve yönetim panelinin varsayılan değerinde.
8. Telefonda düşük güç modunda açılan yedek (düz) lastik sahnesi sağdan taşıyordu. Mobilde ortalandı, kısa ekranlarda biraz aşağı alındı.
9. Google Search Console: URL ön eki mülkü olarak eklendi. HTML meta etiketi ile doğrulandı.

## Sırada olanlar (Mustafa yapacak)
- [ ] Search Console'da Site haritaları bölümüne `sitemap.xml` gönder.
- [ ] Ertesi gün "Dizine eklenmesini iste"yi tekrar dene. İlk gün "Kota aşıldı" hatası verdi.
- [ ] Birkaç gün sonra Google'da `site:citak-oto-lastik.vercel.app` ara.
- [ ] Google İşletme Profili aç (business.google.com): adres, telefon, site linki, kategori olarak "Lastikçi" ve "Yol yardım hizmeti".
- [ ] Ana ekran kısayolunu silip yeniden ekle, yeni simge görünsün.

## İsteğe bağlı
- Kendi alan adı (ör. citakotolastik.com). Ücretli, onay gerekiyor.
- Yol Yardım QR etiketini yeni adresle güncellemek.
- Ayrıntıları henüz verilmedi: hizmet bölgesi, tamir ve 2. el lastik detayları.
