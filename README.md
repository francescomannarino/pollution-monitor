# 🌍 SDS011 Air Quality Monitor

Un sistema completo per il monitoraggio della qualità dell'aria in tempo reale utilizzando il sensore SDS011, con interfaccia web moderna e dashboard interattiva.

## 📋 Caratteristiche

- **Monitoraggio in tempo reale** dei livelli di PM2.5 e PM10
- **Dashboard web moderna** con grafici interattivi
- **Indicatori di qualità dell'aria** basati su standard internazionali
- **Archiviazione dati** in formato CSV e JSON
- **Statistiche automatiche** con medie su 24 ore
- **Design responsive** ottimizzato per desktop e mobile
- **Aggiornamento automatico** dei dati ogni 10 minuti

## 🛠️ Componenti

### Hardware Richiesto
- **Sensore SDS011** (Nova Fitness) per rilevamento particolato
- **Raspberry Pi** o computer Linux con porta USB
- **Cavo USB-TTL** per connessione sensore

### Software
- **Python 3.x** con librerie pyserial
- **Web server** per servire l'interfaccia (nginx, Apache, o Python http.server)
- **Browser moderno** per visualizzare la dashboard

## 📊 Utilizzo

### Funzionalità Dashboard
- **Valori correnti**: PM2.5 e PM10 in tempo reale
- **Indicatore qualità**: Colore e livello di qualità dell'aria
- **Statistiche 24h**: Medie giornaliere automatiche
- **Grafici interattivi**: Andamento temporale con zoom
- **Controlli**: Aggiornamento manuale e cambio periodo


## 📈 Livelli di Qualità dell'Aria

| PM2.5 (μg/m³) | Livello | Colore | Descrizione |
|---------------|---------|--------|-------------|
| 0-15 | Buona | 🟢 Verde | Aria pulita |
| 16-25 | Moderata | 🟡 Giallo | Accettabile |
| 26-50 | Sensibile | 🟠 Arancione | Attenzione gruppi sensibili |
| 51-75 | Malsana | 🔴 Rosso | Evitare attività all'aperto |
| 76+ | Molto malsana | 🟣 Viola | Pericoloso per tutti |


## 📝 API Dati

### Endpoint Disponibili
- `data/latest.json` - Ultimo valore e statistiche
- `data/pollution_data.json` - Dati storici completi
- `data/pollution_data.csv` - Dati storici in formato CSV

### Formato JSON Latest
```json
{
  "last_update": "2024-01-15T10:30:00",
  "current": {
    "pm25": 15.2,
    "pm10": 23.1,
    "quality": {
      "level": "Buona",
      "color": "#00e400"
    }
  },
  "stats": {
    "pm25": {
      "avg_24h": 18.5,
      "max_24h": 45.2,
      "min_24h": 8.1
    }
  }
}
```

## 🤝 Contribuire

1. Fork del repository
2. Crea branch per feature (`git checkout -b feature/nuova-funzione`)
3. Commit delle modifiche (`git commit -am 'Aggiunge nuova funzione'`)
4. Push del branch (`git push origin feature/nuova-funzione`)
5. Crea Pull Request

## 📜 Licenza

Questo progetto è rilasciato sotto licenza MIT. Vedi il file `LICENSE` per i dettagli.

## 🔗 Collegamenti Utili

- [Specifiche Sensore SDS011](https://cdn-reichelt.de/documents/datenblatt/X200/SDS011-DATASHEET.pdf)
- [Standard WHO Qualità dell'Aria](https://www.who.int/news-room/fact-sheets/detail/ambient-(outdoor)-air-quality-and-health)
- [Chart.js Documentation](https://www.chartjs.org/docs/)

## 👨‍💻 Autore

Creato con ❤️ per il monitoraggio ambientale

---

⭐ **Se questo progetto ti è utile, lascia una stella su GitHub!** ⭐