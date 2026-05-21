# 🎯 Ultrasonic Radar – Arduino UNO

> **Digitális Technika II. – Projektfeladat**  
> Neumann János Egyetem, Műszaki és Informatikai Kar

---

## 📡 A projektről

Egy ultrahangos radarrendszer, amely **Arduino UNO** mikrovezérlővel, **HC-SR04** ultrahangos szenzorral és **SG90** szervómotorral valósítja meg a 15°–165° közötti tér pásztázását. A projekt **TinkerCAD** szimulátorban készült, és egy webalapú valós idejű vizualizációval egészül ki.

---

## ⚙️ Felhasznált alkatrészek

| Alkatrész | Típus | Szerep |
|---|---|---|
| Mikrovezérlő | Arduino UNO | Vezérlés |
| Ultrahangos szenzor | HC-SR04 | Távolságmérés |
| Szervómotor | SG90 | Pásztázás |
| LED – zöld | 5 mm | Szabad zóna (> 50 cm) |
| LED – sárga | 5 mm | Közel zóna (20–50 cm) |
| LED – piros | 5 mm | Veszély zóna (< 20 cm) |
| Hangjelző | Passzív buzzer | Hangriasztás |

---

## 🚦 Riasztási szintek

```
d > 50 cm   →  🟢 Zöld LED  |  Nincs hangjelzés
20–50 cm    →  🟡 Sárga LED |  500 Hz, 50 ms impulzus
d < 20 cm   →  🔴 Piros LED |  1000 Hz, 100 ms impulzus
```

---

## 📁 Fájlok

| Fájl | Leírás |
|---|---|
| `radar.ino` | Arduino forráskód |
| `index.html` | Webalapú radar vizualizáció |
| `radar_dokumentacio.pdf` | Projektdokumentáció (PDF) |
| `radar_dokumentacio.docx` | Projektdokumentáció (Word) |

---

## 🖥️ Radar vizualizáció

Az `index.html` egy katonai radar stílusú, valós idejű vizualizáció:

- 🟢 Söprési vonal utóvilágítással
- 💡 Objektumok felvillannak, majd lassan elhalványulnak
- 📊 Élő adatpanel: szög, távolság, állapot
- 🔌 Web Serial API – valódi Arduino közvetlenül csatlakoztatható
- 🎮 Demo mód – Arduino nélkül is bemutatható

> A vizualizáció megnyitásához töltsd le az `index.html` fájlt és nyisd meg **Chrome** vagy **Edge** böngészőben.

---

## 🔌 Pin-kiosztás

| Arduino Pin | Eszköz |
|---|---|
| D2 | Zöld LED |
| D3 | Sárga LED |
| D4 | Piros LED |
| D5 | Piezo buzzer |
| D9 | HC-SR04 TRIG |
| D10 | HC-SR04 ECHO |
| D11 (PWM) | SG90 szervó |

---

## 🛠️ Szimuláció

A projekt **TinkerCAD** online szimulátorban készült.  
🔗 [TinkerCAD projekt megnyitása](https://www.tinkercad.com/things/3AQ8CRyIPmM-neat-stantia-kup/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=QiqKBnkvd7oX4_z7DgXdvyDAWPgGGusEn3fMujofIpw) 

---

## 📄 Dokumentáció

A teljes projektdokumentáció (10+ oldal) tartalmazza:
- Feladat leírása és funkcionalitás
- Áramköri kapcsolás és pin-kiosztás
- Programkód magyarázata
- Tesztesetek és eredmények
- Felhasznált irodalom

---

*Neumann János Egyetem – AMF | 2025/2026. tanév, 2. félév*
