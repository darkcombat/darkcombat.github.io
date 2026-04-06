# Guida e Testo per App Review Meta: "Page Public Content Access"

## 1. Testo Giustificativo (Copia e incolla nel modulo Meta)

**Fornisci una descrizione dettagliata del modo in cui la tua app usa l'autorizzazione...**

> "La nostra applicazione "MASE - Osservatorio del Cittadino" utilizza la funzione "Page Public Content Access" per aggregare, analizzare e visualizzare esclusivamente i post pubblici diramati da specifiche Pagine Facebook di natura istituzionale (es. enti della Protezione Civile, Comuni, dipartimenti governativi), per le quali non abbiamo un ruolo di amministrazione diretta.
>
> L'app preleva questi dati in sola lettura (esclusivamente testo del post, timestamp e nome/ID della Pagina attraverso l'endpoint GET /page-id/feed) passandoli attraverso un nostro Engine di Intelligenza Artificiale proprietario per la classificazione del linguaggio naturale (NLP). 
> 
> Questo uso **migliora enormemente l'esperienza** dell'operatore umano di pubblica sicurezza che usa la nostra app: in situazioni di calamità, invece di dover monitorare manualmente decine di Pagine pubbliche di comuni diversi sparute sul web, l'operatore riceve in un'unica dashboard un feed centralizzato dove i post istituzionali sono già estratti, raggruppati tempestivamente e classificati per gravità (es. Allerta Rossa = IDROGEOLOGICO). L'operatore può quindi avviare le procedure di escalation con un clic, riducendo drasticamente i tempi operativi di reazione ai disastri.
>
> L'autorizzazione è **strettamente necessaria per il funzionamento** dell'app: il sistema di allerta del nostro software si basa esattamente sull'analisi passiva e in real-time dei comunicati d'emergenza rilasciati sui social network dagli enti sul territorio nazionale. Senza l'accesso in ricerca ai contenuti pubblici delle Pagine istituzionali non di nostra proprietà, l'intero cruscotto sarebbe privo della materia prima fondamentale per rilevare le allerte ambientali e l'app perderebbe la sua funzione primaria."

---

## 2. Script per la Registrazione dello Schermo (Video di 1-2 minuti)

In base alla dashboard `index.html` che ti ho costruito, ecco letteralmente i passi e le mosse (choreography) da eseguire durante la registrazione dello schermo. 
*Nota: Puoi registrare l'audio leggendo i testi suggeriti in inglese (Meta preferisce review in inglese pur accettando altre lingue) o limitarti a far capire ai revisori le tue intenzioni col mouse.*

**Setup preliminare:**
1. Prepara il registratore (OBS, Loom, Quicktime...).
2. Apri il file `index.html` nel browser a pieno schermo.
3. Fai partire la registrazione.

**Registrazione - Azione 1: Lo scopo dell'app (15 sec)**
- **Azione:** Muovi il cursore sui 3 riquadri in alto (I KPI "Pagine Monitorate", "Post Analizzati").
- **Voiceover suggerito:** *"Hello Meta Review Team. This is the government dashboard 'MASE Citizen Observatory'. We are requesting 'Page Public Content Access' to aggregate crisis updates published on Facebook by public city councils and civil protection departments without needing page admin rights."*

**Registrazione - Azione 2: Mostrare l'uso dei dati (20 sec)**
- **Azione:** Vai nella sezione "Feed Allerte in Tempo Reale". Clicca sul pulsante blur col simbolo di aggiornamento in alto a destra **"Aggiorna"**. (Mostrerà lo spinner e poi comparirà la notifica verde di sincro in basso a destra).
- **Voiceover suggerito:** *"The system fetches public post feeds via Graph API v18.0. As you can see, we display the Page Name, the exact publish time, and the raw text message of the extreme weather alert."*

**Registrazione - Azione 3: Prova tecnica (Punto cruciale che farà approvare l'app) (25 sec)**
- **Azione:** Sotto il primo alert (Comune di Genova), clicca sull'opzione **"Dati Meta Raw (JSON)"**. Si aprirà il nostro bellissimo modal oscuro ideato appositamente per loro.
- **Azione:** Muovi lentamente il cursore evidenziando il path verde in alto `GET /v18.0/{page-id}/feed` e poi seleziona le prime righe del payload JSON dimostrando l'array di dati che ci prendiamo (`"message"`, `"from.name"`).
- **Voiceover suggerito:** *"We only read public properties. Here is the mock JSON payload. We don't write anything back to Facebook. We only capture the 'message' text to feed our NLP engine which assesses the threat level (e.g. Red Alert)."*
- **Azione:** Clicca su "Chiudi Visualizzatore".

**Registrazione - Azione 4: Esperienza Utente (15 sec)**
- **Azione:** Mostra come l'app gestisce i dati scaricati. Sulla terza scheda in basso (Comune di Milano), clicca **"Ignora / Rimuovi"**. L'animazione cancellerà l'alert e il contatore in alto scenderà da 3 a 2.
- **Voiceover suggerito:** *"By displaying relevant crisis posts in a single dashboard, human operators can rapidly dismiss false alarms or escalate real threats, drastically reducing reaction time during natural disasters."*

**Fine Registrazione.** (Stop al video).
