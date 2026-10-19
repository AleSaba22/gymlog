# GymLog Web

Web app installabile (PWA) per schede pesi, registrazione carichi e ripetizioni per serie, storico, progressi fisici, importazione CSV e backup JSON.

## Funzioni
- Crea e modifica schede e relativi esercizi.
- Registra kg, ripetizioni e serie completate in ogni allenamento.
- Mostra l'ultimo carico registrato per esercizio e lo storico delle sessioni.
- Registra peso, torace, vita, addome, fianchi, braccio, coscia, polpaccio e massa grassa.
- Importa CSV con colonne `Scheda,Esercizio,Serie,Ripetizioni`.
- Esporta e ripristina un backup JSON.
- Service worker per il funzionamento offline dopo il primo caricamento.

## Prova sul PC
Per un test rapido, apri `index.html` nel browser. Il salvataggio funziona, ma l'installazione PWA/offline richiede un sito servito via HTTPS o localhost.

## Pubblicazione gratuita con GitHub Pages
1. Crea o accedi a un account GitHub.
2. Crea un repository pubblico, ad esempio `gymlog`.
3. Carica tutti i file di questa cartella nella radice del repository.
4. Vai in **Settings → Pages**.
5. Scegli **Deploy from a branch**, seleziona `main` e `/ (root)`, poi salva.
6. Attendi la pubblicazione e apri l'indirizzo HTTPS indicato da GitHub Pages.

## Installazione su iPhone
1. Apri il link HTTPS pubblicato in **Safari**.
2. Tocca **Condividi** → **Aggiungi alla schermata Home**.
3. Conferma con **Aggiungi**.
4. Apri GymLog dall'icona. Dopo il primo caricamento il service worker memorizza i file per l'uso offline.

## Privacy e dati
I dati delle schede, sessioni e misure sono salvati in `localStorage` del browser sul dispositivo. L'app non invia i dati a un server. La pubblicazione su GitHub Pages ospita solo i file dell'app, non i dati personali inseriti. Esporta regolarmente il backup JSON. Se cancelli i dati di Safari, cambi browser o dispositivo, i dati locali potrebbero andare persi.

## Limiti attuali
- L'importazione è CSV; i PDF non vengono interpretati in questa versione.
- Le foto di progressione, i grafici storici avanzati delle circonferenze e il timer recupero non sono ancora inclusi.
- I dati locali non si sincronizzano automaticamente tra dispositivi.
- Questo è un prototipo iniziale: testare importazione, backup e flussi su PC e iPhone prima di usarlo come unico archivio.

## CSV di esempio
```csv
Scheda,Esercizio,Serie,Ripetizioni
Scheda A,Panca piana,4,8
Scheda A,Squat,4,8
Scheda A,Lat machine,3,12
```
