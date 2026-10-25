# Safety 4.0 Bootcamp – Argesta Palet Streç Sarma Makinesi

**Öğrenci:** Furkan Akkamış – 235542002
**Bölüm:** Teknoloji Fakültesi – Yazılım Mühendisliği
**Makine:** Argesta Makine Mühendislik A.Ş. – Döner Tablalı Otomatik Palet Streç Sarma Makinesi

Bu repo, ilk 4 haftanın laboratuvar föylerinin seçilen makineye uygulanmış **kör test cevaplarını** içerir.

## İçerik

| Hafta | Laboratuvar | Çıktı | Evidence Pack |
|---|---|---|---|
| 1 | [Safety Architecture](labs/lab1-safety-architecture.md) | Safety Function Map | EP 03 |
| 2 | [IEC 62443 Mini Workshop](labs/lab2-iec62443.md) | Zone / Conduit Diagram | EP 05 |
| 3 | [Threat & Risk + Risk Matrix](labs/lab3-risk-matrix.md) | Risk Register | EP 04 |
| 4 | [Secure Remote Access](labs/lab4-secure-remote-access.md) | Secure Architecture | EP 02 + EP 06 |

## Makine özeti

Makine, palet üzerindeki yükü döner tabla ile çevirirken film taşıyıcının yukarı-aşağı hareketiyle streç film sarar ve sarma sonunda filmi keser.

- Çalışma modu: otomatik / manuel
- Kontrol: PLC + dokunmatik operatör paneli (HMI)
- Maks. sarma yüksekliği: 2.700 mm · Maks. palet ağırlığı: 2.000 kg
- Çift motorlu ön gerdirme, mekanik fren, otomatik hatta entegrasyon

**Tehlikeli hareketler:** döner tabla, film taşıyıcı (dikey hareket), film kesme/tutma ünitesi, yük devrilmesi.

## Varsayımlar

Üretici kataloğunda emniyet ve ağ altyapısı ayrıntılı verilmediği için aşağıdakiler varsayılmıştır:

1. Makine hat içi (inline) çalışır; çevresinde çit, kilitli bakım kapısı ve palet giriş/çıkışında muting'li ışık perdesi vardır.
2. Emniyet zinciri: ışık perdesi + kapı kilidi + E-stop → Safety PLC → STO / kontaktör.
3. Makineye sonradan internete açık bir **uzak bakım modülü** eklenmiştir.

## Kaynaklar

- [Argesta – ürün sayfası (DirectIndustry)](https://www.directindustry.com/prod/argesta-makina/product-4620456-2863448.html)
- [Argesta – ürün kataloğu (PDF)](https://pdf.directindustry.com/pdf/argesta-makina/product-catalog/4620456-1151936.html)

> Bu bir eğitim çıktısıdır, resmî denetim değildir.
