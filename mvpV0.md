# 📌 DOCUMENTO FUNZIONALE MVP – IRONMATH (VERSIONE BETA)

## **A. OBIETTIVO DELLA BETA**

PREAVVISO: tutte le considerazioni fatte in questo documento sono nell'ottica di un pubblico al 95% minorenne, ergo tenere in considerazione che studenti maggiorenni non risentono minimamente delle restrizioni di cui parleremo...

L'MVP di IRONMATH ha lo scopo di snellire il carico progettuale a fronte di molteplici migliorie future.

E' per questo che la web app, almeno inizialmente, si rivolgerà unicamente agli studenti di scuola media, e quindi coprirà solo il programma di matematica, relegando i 5 anni di liceo e la fisica a una versione futura.

Cionostante si pone come main goal la certezza di essere totalmente funzionante sia nei confronti dello studente, che del/dei genitore/i, che del docente di matematica.

Ergo il punto di partenza è che sono previsti 3 ruoli/"account-level" distinti:

1. **Studente**
2. **Genitore**
3. **Docente**

Ogni ruolo accede tramite login e ha una dashboard dedicata. 

Partiamo chiaramente dal lato studente, snocciolando tutto quello che deve essere in grado di fare/vedere/...

###Lo studente, con l'MVP, deve essere in grado di:**

### **1) Effettuare la registrazione al sito (STUDENTE):

- Tale registrazione non parte mediante il classico bottone "Registrati/Accedi". iI flusso è molto più lineare e non prevede di "cercare" i bottoni per proseguire:

	1) L'utente "atterra" nella landing page e nel main di essa sceglie tramite bottoni enormi che fanno progredire espandendo dinamicamente verso il basso:

		a) classe di appartenenza (prima, seconda o terza media) che farà da tara per l'anno corrente e il/i precedente/i;

		b) la situazione scolastica/motivo di iscrizione: studente già eccelso che vuole consolidare/portarsi avanti/eccellere oppure più genericamente il classico studente in difficoltà che non vuole il debito (non importa se ambisce a passare con il 6 politico senza debiti estivi o se vuole migliorare oltre il 7 - per ora, poi su questo si ragionerà molto più in là per una profilazione avanzata).

		c) sotto a tali sezioni ci sarà un'altra coppia di bottoni "Sei docente/Sei genitore? Clicca qui... o simile" Ergo il default form è chiaramente quello dello studente

	Dopo aver selezionato tali due dati essenziali, la registrazione prosegue come usualmente dovrebbe in un qualsiasi altro sito:
		
	2) Campi richiesti

		- **Username** (visibile nell’app, quello che l'IA saluta, nessun nominativo in chiaro!)

		- Data di nascita che valida automaticamente la maggiore età dell'utente che vuole registrarsi:
			
			in caso di maggiore età disabilita il campo di email genitore/tutore e redireziona la mail di avvenuta registrazione alla mail personale; 
			
			in caso di utente minore, si attiva il campo di mail genitore/tutore e la mail di conferma registrazione viene redirezionata all'indirizzo del suddetto genitore/tutore;

		- **Email studente** (*dovrebbe preferenzialmente essere la mail scolastica ufficiale dell'istituto, in vista di una virata verso il B2B, ma anche la personale va bene. Chiaramente se lo studente usa IronMath in seguito a un accordo di B2B tra scuola e IronMath, allora e solo allora la mail scolastica diventa tassativa!*)

		- **Email genitore/tutore** (OBBLIGATORIA per tutti gli utenti in quanto tutti tendenzialmente minorenni)
				
		- **Password**
		- **Conferma password**

		- ✅ “Ho letto e accetto Termini & Condizioni”
		- ✅ “Ho letto e accetto l'Informativa sulla Privacy”

		- ENORME TASTO REGISTRATI, alla cui pressione si attiva il flusso concreto di registrazione di seguito riportato...

	Quando si clicca su "REGISTRATI", il form scompare e viene rimpiazzato con un placeholder di attesa, del tipo "Registrazione completata. Controlla la casella di posta elettronica del tuo genitore/tutore che hai inserito poc'anzi, o chiedigli direttamente di approvare il completamento dell'iscrizione o tuffati in IronMath con un account non limitato (ti manderemo reminder di completare la registrazione effettiva)".

	Lo studente è davanti a un bivio: può approvare/far approvare al genitore l'email di attivazione completa dell'account, o continuare con account limitato.
	
	Dopodiché, l'utente riceverà, a prescindere dall'età, una mail di attivazione account:

	- La mail per il genitore/tutore dovrà spiegare brevemente nel corpo stesso il principio etico per cui è nata la piattaforma IronMath, con possibile link a video youtube di presentazione ufficiale;
	- Dichiara esplicitamente i dati raccolti dell'utente con link a informativa privacy, termini e condizioni...;
	-  DUE BOTTONI LINK: APPROVO/DECLINO ISCRIZIONE DI MIO FIGLIO AD IRONMATH
		- Se il genitore clicca **APPROVO**:
			  - Account studente → **COMPLETO**
			  - Dati iniziano ad essere salvati
			  - Viene creato l’account genitore

		- Se il genitore clicca **NON APPROVO**:
			  - Account resta limitato
			  - Può essere cancellato dopo 15 giorni (*)

VEDIAMO I DUE SCENARI:

**SCENARIO 1: STATO INIZIALE LIMITATO**

- Può fare solo 2–3 esercizi demo
- Nessun salvataggio permanente
- Nessuna profilazione di alcun tipo
- Nessun accesso a progressi/statistiche

Lo sblocco richiede approvazione della suddetta mail arrivata al genitore

**SCENARIO 2: STATO INIZIALE COMPLETO**

- Se l'utente ha effettivamente ricevuto l'approvazione del genitore via mail, allora avrà il suo account totalmente completo, con tutta la profilazione attiva che ci prefissiamo per la beta e che sarà oggetto di trattamento specifico tra un po'.
- L'account genitore è del tutto parallelo a quello del figlio studente.

IN OGNI CASO, DOPO L'APPROVAZIONE VIA MAIL / DOPO IL BOTTONE "OPPURE ACCEDI CON ACCOUNT LIMITATO", LO STUDENTE VIENE RENDIRIZZATO AL FORM DI LOGIN STANDARD, PER POTER AVERE

1) Subito una seconda barriera di sicurezza post-registrazione;
2) Fargli prendere immediatamente dimestichezza con l'UI di login che si ritroverà di lì in avanti ad accoglierlo.


### **2) Login (STUDENTE)**

Campi del form:

- Ambivalente:
	a) email, sia essa scolastica o personale, ma l'importante è che sia quella dello studente, non del genitore;
	b) oppure direttamente l'username che lo studente ha scelto e con cui sarà salutato in-app;
	
- Password

Da capire se da implementare subito o in un futuro prossimo (io proporrei subito per questioni meramente di accessibilità - i giovani non si segnano le password in cartaceo/sono diffidenti a lasciarle su portafogli ICloud o simili):

- Hyperlink "Hai dimenticato la password?" - con procedura recupero standardizzata;
- CheckBox "Ricordami" ✅ per login rapido dalla sessione corrente in avanti fino a esplicito un-check della medesima;

Dopo tale compilazione, lo studente finalmente accede e ri-atterra in una landing page post-autenticazione.

Da qui lo studente sarà in grado di usufruire di tutti i servizi della 

---


- Permettere a uno studente di svolgere esercizi di matematica su **un solo modulo** (es. “Equazioni di primo grado”).
- Registrare errori, tentativi e progressi.
- Permettere a genitori e docenti di monitorare le performance.
- Gestire l'accesso dei **minori** in modo conforme e responsabile.

La beta NON deve includere tutte le funzionalità finali; deve essere stabile, semplice e utilizzabile.





## 3.4 DASHBOARD STUDENTE (ACCOUNT COMPLETO)

Elementi visualizzati:

- Messaggio di benvenuto
- “Continua da dove hai lasciato”
- Modulo disponibile:
  - “Algebra – Equazioni di primo grado”
  - Pulsante **Inizia**
- Landing page con due sezioni ai lati per tornare al topic precedente e parte centrale per vedere i tuoi progressi sotto forma di grafico, invece per la parte a destra la solita dashboard con tutte le azioni

### Sezione progressi (base)

- Numero esercizi completati
- Percentuale risposte corrette
- Tempo totale di studio (*opzionale*)
- (*in futuro, percentuale risposte errate per evidenziare lacune dell'utente*)

### Menu

- Esercizi
- Progressi, ci devono essere degli schemi facili da leggere
- Profilo
- Logout

---

## 3.5 SCHERMATA ESERCIZI

Elementi:

- Enunciato
- Campo risposta

### Pulsanti

- **Conferma risposta**
- **Riprova**
- **Chiedi un indizio**
- **Mostra soluzione** (*limitata o disattivata nella beta*)
- **Salta esercizio**
- **Aiuto** -- per evidenziare i problemi che l utente già conosce sulla sua formazizone, cosi da risviluppare una roadmap più adeguata

### Feedback

- Corretto → Messaggio (di incoraggiamento) + **Prossimo esercizio**
- Sbagliato → Messaggio (perchè hai sbagliato, a seconda dell'errore viene indicata una lacuna e ti viene suggerito un modulo da rivedere dall'llm) + Riprova

### Dati registrati

- corretto/sbagliato
- numero tentativi
- tempo impiegato
- indizi richiesti
- esercizi saltati

---

## 3.6 RIEPILOGO SESSIONE

Mostra:

- Numero esercizi svolti
- % corrette
- Errori comuni

Pulsanti:

- “Nuova sessione”
- “Torna alla dashboard”

---

## 3.7 SEZIONE “PROGRESSI STUDENTE”

Beta (semplice):

- Numero esercizi totali
- % corrette
- Stato modulo:
  - Non iniziato / Base / Intermedio / Solido

*In futuro*: Grafici, trend, report avanzati (*)

---

# ✅ 4. FUNZIONALITÀ GENITORE

L’accesso è possibile solo dopo approvazione.

## 4.1 CREAZIONE ACCOUNT GENITORE

- Automatica dopo approvazione
- Oppure manuale (*)

Dashboard genitore mostra:

- Nome studente
- Modulo attivo
- Numero esercizi svolti
- % corrette
- Errori ricorrenti (testo semplice)

*In futuro*: notifiche, report PDF, suggerimenti (*)

---

# ✅ 5. FUNZIONALITÀ DOCENTE

## 5.1 REGISTRAZIONE DOCENTE

Campi:

- Nome
- Cognome
- Email
- Password
- Nome scuola (*)

## 5.2 DASHBOARD DOCENTE

Mostra:

- Le sue classi
- Numero studenti per classe
- % corrette media

## 5.3 CREAZIONE CLASSE

Il docente può:

- Creare classe
- Generare **codice classe**
- Condividerlo agli studenti

## 5.4 DETTAGLIO CLASSE

Mostra per ogni studente:

- Nome/Nickname
- Esercizi completati
- % corrette
- Stato modulo

*In futuro*: compiti assegnati, chat, analytics avanzati (*)

---

# ✅ 6. ELEMENTI COMUNI

- Logo IRONMATH
- Layout responsive
- Logout
- Password criptate (obbligatorio)
- Accessi basati su ruoli

*In futuro*: Dark mode, Mobile App, Gamification (*)

---

# ✅ 7. COSA È OBBLIGATORIO NELLA BETA

- Registrazione con nickname + email genitore
- Account limitato senza approvazione
- Consenso genitore via email
- 1 modulo di esercizi funzionante
- Tracciamento base risultati
- Dashboard studente semplice
- Dashboard genitore semplice
- Dashboard docente base
- Ruoli separati

---

# ✅ 8. COSA PUÒ ESSERE OMESSO (*) NELLA BETA

- Reset password (*)
- Profilo avanzato studente (*)
- Grafici complessi (*)
- Mostra soluzione completa (*)
- Report dettagliati (*)
- Data di nascita automatica (*)
- Notifiche (*)
- Più moduli didattici (*)
- Gamification (*)
- Pagamenti/piani premium (*)
- Chat AI (*)
- Creazione esercizi da parte docente (*)

---

# ✅ 9. VISIONE TECNICA (ALTO LIVELLO)

### Backend

- Gestione ruoli
- Collegamento studente–genitore–docente
- Tracciamento prestazioni
- Stato account limitato/completo

### Frontend

- UI dashboard
- UI esercizi
- UI registrazione/login

### Database (tabelle minime)

- Utenti
- Relazione studente–genitore
- Relazione studente–classe–docente
- Esercizi
- Risultati esercizi

*In futuro*: logging avanzato, dataset AI, export, modelli NLP (*)

---

# ✅ 10. TONO DELL’APP

- Positivo
- Motivante
- Semplice
- Non giudicante

---

## ✅ DOCUMENTO PRONTO PER IL DEV
