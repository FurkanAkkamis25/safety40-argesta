# SWOT Analizi – Emniyet ve Siber Güvenlik Durumu

Lab 1–7 bulgularına dayanır. Her makine için emniyet (safety) ve siber güvenlik (security) açısından hazırlanmıştır.

## 1. Argesta Döner Tablalı Palet Streç Sarma Makinesi

| | |
|---|---|
| **Güçlü yönler (S)** | • Ayrı emniyet yolu: ışık perdesi + kapı kilidi + E-stop → Safety PLC → STO (Lab 1)<br>• PLr d hedefi, taşıyıcıda mekanik fren (düşmez)<br>• Safety PLC ayrı bölgede (Z5), yalnız durum okunur (Lab 2)<br>• Basit, az bileşenli kontrol yapısı → SBOM takibi kolay |
| **Zayıf yönler (W)** | • İnternete açık uzak bakım modülü, ortak servis hesabı, MFA ve kayıt yok (Lab 3–4)<br>• Kilitsiz USB ile limit ayarı değiştirilebilir (Lab 3)<br>• Muting ayarları dijital olarak değiştirilebilir<br>• Katalogda emniyet/ağ bilgisi yok; birçok konu varsayıma dayanıyor |
| **Fırsatlar (O)** | • Jump server + VPN + MFA + kişisel hesap ile güvenli uzak erişim (Lab 4)<br>• SBOM ve CVE takibiyle planlı yama yönetimi (Lab 5)<br>• CRA uyumu, üreticiye ihracatta rekabet avantajı sağlar (Lab 6)<br>• YZ destekli sarma kalite kontrolü, film tasarrufu (Lab 7) |
| **Tehditler (T)** | • Uzak modül üzerinden muting değişikliği → kol sıkışması (risk 18, Lab 3)<br>• PLC firmware'inde kritik CVE (CVSS 9.8, Lab 5)<br>• Fidye yazılımının HMI'ı kilitlemesi → gevşek sarım, yük devrilmesi<br>• Manipüle edilmiş kamera girdisi ile yanlış YZ kararı (Lab 7)<br>• CRA bildirim sürelerinin (24 s / 72 s / 14 gün) kaçırılması |

**Öncelikli aksiyon:** Uzak bakım modülünü DMZ'ye alıp jump server + MFA arkasına koymak; USB portlarını kilitlemek.

## 2. Şişeleme Hattı

| | |
|---|---|
| **Güçlü yönler (S)** | • Koruyucu kapı, ışık perdesi, E-stop → Safety PLC → STO<br>• Bölgelere ayrılmış ağ, Safety PLC ayrı bölgede |
| **Zayıf yönler (W)** | • Paylaşılan VPN/servis parolası, internetten doğrudan IPC erişimi<br>• Çok bileşenli hat (karusel, kapatıcı, robot) → geniş saldırı yüzeyi |
| **Fırsatlar (O)** | • Merkezi oturum kaydı ve kişisel hesaplar<br>• Görüntü işleme ile dolum/kapak kontrolü |
| **Tehditler (T)** | • Muting süresinin uzatılması → parmak kaybı<br>• USB ile robot hız/alan sınırlarının değiştirilmesi |

## 3. PaketPro 3000 Paketleme Makinesi

| | |
|---|---|
| **Güçlü yönler (S)** | • Işık perdesi + kapak kilidi ile korunan sıcak çene ve bıçak<br>• Emniyet PLC'si ayrı |
| **Zayıf yönler (W)** | • Varsayılan admin/admin hesabı, HMI'da şifresiz HTTP (port 80)<br>• Kartonda yazılı Wi-Fi parolası, kilitsiz USB |
| **Fırsatlar (O)** | • Uzak bakım modülünün DMZ'ye alınması, HTTPS ve USB kilitleme<br>• Bulut telemetrisiyle kestirimci bakım |
| **Tehditler (T)** | • İnternete açık uzak bakım modülünden yetkisiz giriş<br>• Çene sıcaklığı/bıçak ayarlarının değiştirilmesi → yanık, kesilme |

> Bu bir eğitim çıktısıdır, resmî denetim değildir.
