# India-Stocks-1411-1440-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1411 to 1440)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1411-1440-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1411 to 1440)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1411 | `JTEKTINDIA` | Jtekt India Limited | `JTEKTINDIA.NS` |
| 1412 | `JTLIND` | JTL INDUSTRIES LIMITED | `JTLIND.NS` |
| 1413 | `JUBLCPL` | Jubilant Agri and Consumer Products Limited | `JUBLCPL.NS` |
| 1414 | `JUBLPHARMA` | Jubilant Pharmova Limited | `JUBLPHARMA.NS` |
| 1415 | `JUNIPER` | Juniper Hotels Limited | `JUNIPER.NS` |
| 1416 | `JUSTDIAL` | Just Dial Limited | `JUSTDIAL.NS` |
| 1417 | `JYOTHYLAB` | Jyothy Labs Limited | `JYOTHYLAB.NS` |
| 1418 | `JYOTIRES` | Jyoti Resins & Adhesives Limited | `JYOTIRES.NS` |
| 1419 | `JYOTISTRUC` | Jyoti Structures Limited | `JYOTISTRUC.NS` |
| 1420 | `KABRAEXTRU` | Kabra Extrusion Technik Limited | `KABRAEXTRU.NS` |
| 1421 | `KAKATCEM` | Kakatiya Cement Sugar & Industries Limited | `KAKATCEM.NS` |
| 1422 | `KALAMANDIR` | Sai Silks (Kalamandir) Limited | `KALAMANDIR.NS` |
| 1423 | `KALPATARU` | Kalpataru Limited | `KALPATARU.NS` |
| 1424 | `KALYANI` | Kalyani Commercials Limited | `KALYANI.NS` |
| 1425 | `KALYANIFRG` | Kalyani Forge Limited | `KALYANIFRG.NS` |
| 1426 | `KAMAHOLD` | Kama Holdings Limited | `KAMAHOLD.NS` |
| 1427 | `KAMANWALA` | Kamanwala Housing Construction Limited | `KAMANWALA.NS` |
| 1428 | `KAMATHOTEL` | Kamat Hotels (I) Limited | `KAMATHOTEL.NS` |
| 1429 | `KAMDHENU` | Kamdhenu Limited | `KAMDHENU.NS` |
| 1430 | `KAMOPAINTS` | Kamdhenu Ventures Limited | `KAMOPAINTS.NS` |
| 1431 | `KANANIIND` | Kanani Industries Limited | `KANANIIND.NS` |
| 1432 | `KANCHI` | Kanchi Karpooram Limited | `KANCHI.NS` |
| 1433 | `KANCOTEA` | Kanco Tea & Industries Limited | `KANCOTEA.NS` |
| 1434 | `KANOHAR` | Kanohar Electricals Limited | `KANOHAR.NS` |
| 1435 | `KANORICHEM` | Kanoria Chemicals & Industries Limited | `KANORICHEM.NS` |
| 1436 | `KANPRPLA` | Kanpur Plastipack Limited | `KANPRPLA.NS` |
| 1437 | `KANSAINER` | Kansai Nerolac Paints Limited | `KANSAINER.NS` |
| 1438 | `KAPSTON` | Kapston Services Limited | `KAPSTON.NS` |
| 1439 | `KARAMTARA` | Karamtara Engineering Limited | `KARAMTARA.NS` |
| 1440 | `KARMAENG` | Karma Energy Limited | `KARMAENG.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream JTEKTINDIA 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1411-1440-Historical-Data/main/JTEKTINDIA/1m/2026/10/JTEKTINDIA_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
