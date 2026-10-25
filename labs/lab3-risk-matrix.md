# Lab 3 – Threat & Risk + Risk Matrix

**Makine:** Argesta Döner Tablalı Palet Streç Sarma · **Çıktı:** Risk Register → EP 04 Risk Assessment

Skor = L × S × E (her biri 1–3) · Kritik 18–27 · Yüksek 9–17 · Orta 4–8 · Düşük 1–3
Kural: S=3 ise skor düşük olsa bile senaryo öne alınır.

## Risk Register

| # | Senaryo (kim → kapı → ne yapar → zincir → fiziksel sonuç) | L | S | E | Skor | Öncelik |
|---|---|---|---|---|---|---|
| 1 | Dış saldırgan → internete açık uzak bakım modülü → Safety PLC'de muting ayarını değiştirir → ışık perdesi devre dışı, operatör filmi bağlarken tabla döner → **kol sıkışması / ezilme** | 2 | 3 | 3 | 18 Kritik | 1 |
| 2 | Ofis çalışanı → phishing → fidye yazılımı HMI'ı kilitler → film gerginliği yanlış kalır, yük gevşek sarılır → forklift taşırken yük devrilir → **hafif yaralanma** | 3 | 1 | 3 | 9 Yüksek | 3 |
| 3 | Bakım personeli → kilitsiz USB → taşıyıcının alt limit ayarını değiştirir → taşıyıcı aşağı iner → **ağır ezilme** | 1 | 3 | 1 | 3 Düşük | 2 |

## Sorular

**1. En yüksek öncelikli senaryonuz hangisi? Neden?**
Senaryo 1 – emniyet fonksiyonunu doğrudan bozuyor ve kalıcı yaralanmaya yol açabilir.

**2. S=3 olup skoru düşük kalan senaryonuz var mı? Nasıl görünür kılacaksınız?**
Evet, Senaryo 3 (skor 3). Kural gereği öne alınır; risk kaydında işaretlenir, USB kilitleme ve limit ayarlarına checksum kontrolü bir sorumluya ve tarihe bağlanır.
