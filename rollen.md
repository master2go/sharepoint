# Rollen- und Rechtearchitektur – SharePoint St. Josef gGmbH

## 1. Hierarchieebenen
- **GLR (Geschaeftsleitungsrunde)**  
  Bestehend aus: GF, Bereichsleitung Kita, HzE, Schule  
- **Bereichsleitungen**  
- **Standortleitungen** (KiTa, HzE, Schulen)  
- **Mitarbeitende / Teams**

---

## 2. Rollen und ihre Rechte

### 🔵 1. GLR – oberste Ebene
**Rechte:**
- Vollzugriff (Owner) auf der Startseite
- Lesen auf allen Bereichs- und Standortseiten
- Optional Bearbeiten bei unternehmensweiten Dokumenten
- Kein operatives Eingreifen in Standortordner

---

### 🟢 2. Bereichsleitung (Kita, HzE, Schule)
**Rechte:**
- Owner ihrer Bereichs-Site
- Lesen auf der Startseite
- Lesen auf anderen Bereichen (optional)
- Bearbeiten auf allen Standortseiten des eigenen Bereichs
- Vollzugriff auf alle "08_Leitung"-Ordner ihres Bereiches

---

### 🟡 3. Standortleitung (z. B. KiTa-Leitung)
**Rechte:**
- Owner der eigenen Standort-Site
- Bearbeiten auf der Bereichs-Site
- Lesen auf der Startseite
- Vollzugriff auf den Standortordner „08_Leitung“
- Bearbeiten in allen Ordnern 01–07

---

### 🟠 4. Teammitglieder
**Rechte:**
- Lesen auf der Startseite
- Bearbeiten auf der eigenen Standort-Site
- Kein Zugriff auf 08_Leitung
- Kein Zugriff auf andere Standorte
- Optional Lesen auf Bereichsebene

---

## 3. Rechte nach Ebene

### A) Startseite (unternehmensweit)
- GLR: Owner  
- Bereichsleitungen: Mitwirken  
- Standortleitungen: Lesen  
- Mitarbeitende: Lesen  

### B) Bereichs-Site (z. B. Kindertagesstaetten)
- Bereichsleitung: Owner  
- GLR: Lesen  
- Standortleitungen: Bearbeiten  
- Mitarbeitende: Lesen (optional)  
- 08_Leitung: Nur Bereichsleitung + GF  

### C) Standort-Site (z. B. Kita 15)
- Standortleitung: Owner  
- Bereichsleitung: Bearbeiten  
- Teammitglieder: Bearbeiten  
- Andere Standorte: Kein Zugriff  
- 08_Leitung: Nur Standortleitung + Bereichsleitung  

---

## 4. Rolle des Ordners „08_Leitung“
- Vererbung wird gebrochen  
- Nur Leitung + Bereichsleitung (optional GF)  
- Ausschließlich vertrauliche Inhalte  
- Keine Teammitglieder  

---

## 5. Rechte-Matrix (kompakt)

| Rolle              | Startseite | Bereich | Standort | 08_Leitung |
|--------------------|------------|---------|----------|------------|
| **GLR**            | Owner      | Lesen   | Lesen    | Optional   |
| **Bereichsleitung**| Lesen      | Owner   | Bearbeiten | Vollzugriff |
| **Standortleitung**| Lesen      | Bearbeiten | Owner   | Vollzugriff |
| **Teammitglied**   | Lesen      | Lesen (opt.) | Bearbeiten | Kein Zugriff |

---

## 6. Saubere technische Umsetzung
- Rollen als **Microsoft-365-Gruppen** anlegen  
- Gruppen auf die jeweiligen Sites mappen  
- 08_Leitung: **immer** eigene Berechtigung, niemals vererbt  
- Möglichst wenige Einzelberechtigungen  
- Rechte werden auf Site-Level definiert, nicht auf Dateiebene
