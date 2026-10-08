# FavoLab: ambito del lancio

8 ottobre 2026. Input: stress test (passo 1, con le soglie go/no-go del §6), brand guide v1 (passo 2), Audit 2 (piano dal codice al lancio). Audit 1 si usa solo dove gli altri tre documenti lo citano o lo contraddicono.

**Come si legge.**
- **Entra**: serve a leggere le soglie del 7 novembre, oppure è un prerequisito di sicurezza o legale senza il quale nessuna famiglia esterna può usare FavoLab. Si fa nelle 20 ore del piano di 30 giorni.
- **Dopo**: si fa solo dopo il GO, con un fattore scatenante misurabile.
- **Non entra**: escluso dal lancio (beta e prima versione pubblica), con il motivo.

---

## 0. Decisioni in breve

1. **Famiglia a €39 senza audio e senza guest mode.** Contiene: favole illimitate, "Scrivi tu cosa è successo", i momenti difficili "gialli" quando un esperto li avrà rivisti, un profilo per ogni figlio, durata fino a 8 minuti, PDF da stampare. L'audio narrato a €39 manda in perdita chi lo usa ogni sera (§2.1). Il valore di questo pacchetto lo misura il test dei soci fondatori (C4).
2. **3 favole gratuite a settimana, salvate per tutti.** 3 è il numero minimo che rende raggiungibile la soglia di attivazione (≥3 favole nella 2ª settimana) e fa vedere il paywall a ogni famiglia attivata. Il salvataggio resta aperto perché il libro si compone con le favole salvate.
3. **Momenti difficili su tre livelli.** Verdi (paure, nido, fratellino, rabbia): aperti a tutti, anche nel piano gratuito, perché portano l'acquisizione. Gialli (separazione, lutto di un nonno o di un animale, ospedale, adozione, bullismo): spenti fino alla revisione dell'esperto, che si paga solo dopo il GO. Rossi: spenti, e alcuni restano fuori per sempre. "Scrivi tu" passa per un classificatore che applica gli stessi tre livelli.
4. **Il nome del bambino resta in FavoLab.** A OpenAI arriva un segnaposto e il nome si inserisce dopo la generazione. Così la promessa "il nome di tuo figlio non va al servizio di AI" diventa vera e il rischio legale principale sparisce per costruzione.
5. **Privacy, termini e consensi minimi prima della prima famiglia in beta.** Nell'Audit 2 erano allo Sprint 3: con la sequenza dello stress test la beta parte prima, quindi i testi legali vanno anticipati. Il consulente arriva dopo il GO, prima del lancio pubblico.

## 1. I criteri usati (stress test, §6)

| Codice | Metrica | GO | STOP | Conta nella regola GO su A? |
|---|---|---|---|---|
| C1 | Attivazione beta: ≥3 favole nella 2ª settimana (n ≥ 30) | ≥30% | <15% | Sì |
| C2 | Sean Ellis "molto deluso" (n ≥ 20) | ≥40% | <25% | No |
| C3 | Preferenza alla cieca contro Gemini (n = 10) | ≥6/10 | ≤3 | Solo per lo STOP |
| C4 | Soci fondatori pagati a €29/anno | ≥3 | 0 | Sì |
| C5 | Registrati organici | ≥20 a settimana | <10 | Sì |
| C6 | Costo per registrazione su Meta | ≤€1 | >€3 | No |
| C7 | Preordini del libro entro il 20/11 | ≥15 | <5 | Decide il PIVOT su B |
| C8 | Costi fissi | ≤€100/mese | >€150/mese | Vincolo |

Vincoli: 5 ore a settimana (20 ore fino al 7 novembre), spesa massima di circa €250 nei 30 giorni, ROI > 0 entro 12 mesi con al massimo €5.000.

**Conseguenza sul calendario.** C1 si misura sulla seconda settimana d'uso. Per averla entro il 7 novembre, una famiglia deve entrare in beta entro il 24 ottobre. Tutto ciò che deve esistere prima della prima famiglia (sicurezza, quota, nome con segnaposto, temi, privacy) va chiuso entro il 20 ottobre.

---

## 2. Incoerenze risolte

### 2.1 Cosa contiene "Famiglia" a €39

**Cosa dicevano i documenti.**

| Voce | Audit 1 | Audit 2 | Brand guide | Decisione |
|---|---|---|---|---|
| Favole illimitate | Sì | Sì | Sì | **Sì**, con un tetto tecnico di 5 al giorno lato server contro gli abusi |
| Momenti difficili | Sì, tutti | Sì, con lucchetto per il gratuito | Paywall "I momenti difficili sono nel piano Famiglia" | **Solo i gialli**, quando saranno rivisti. I verdi sono aperti a tutti (§2.3) |
| Scrivi tu (situazione libera) | Aperto a tutti ("si elimina la chiusura del tema libero") | Lucchetto per il gratuito | Paywall su "Scrivi tu" | **Sì, solo Famiglia** |
| Più profili figlio | Sì | Sì | Sì | **Sì**. Il gratuito ha un profilo |
| PDF da stampare | Sì | Sì ("stampa") | | **Sì** |
| Audio narrato | Sì | Dopo il lancio | Vietato anche nel paywall | **Non entra** a €39 |
| Prova di 7 giorni | Sì | Sì | Sì al lancio, no in beta | **Dopo il GO** (serve il webhook) |

**Perché l'audio resta fuori.** Con le stime dell'Audit 1 (gpt-4o-mini-tts a circa $0,015 al minuto) una favola di 6 minuti costa circa €0,08 di audio. Una famiglia che la ascolta ogni sera spende €2,40 al mese. L'annuale da €39 rende €30,5 netti, cioè €2,54 al mese: l'audio da solo si mangia il 94% del ricavo, prima del testo e dei costi fissi. La cache non aiuta, perché ogni favola è nuova. C'è anche un motivo di marca: la promessa è "da leggere con la tua voce", e una voce sintetica la indebolisce proprio sulla leva che ci distingue da Gemini, che l'audio lo dà già gratis. L'audio potrà rientrare solo con un tetto (10 audio al mese costano circa €0,80) o come aggiunta a pagamento, dopo una misura reale del costo (§3, Dopo).

**Perché il guest mode resta fuori.** Serve l'accesso anonimo di Supabase più Turnstile più il collegamento dell'identità al salvataggio: 4-6 ore su 20, e riapre il fronte delle funzioni AI chiamabili senza account, che l'Audit 1 classifica come critico. Le soglie GO contano i registrati (C5), quindi la prima favola senza account non migliora la metrica che decide. Il problema reale che il guest mode risolveva (le scelte perse prima del login) si copre con il passo 26 dell'Audit 2, che costa meno. Il guest mode torna in gioco se, dopo il lancio pubblico, meno del 40% di chi tocca "Crea la tua prima favola" completa la registrazione.

**€39 basta per questo contenuto?** Oggi nessuno lo sa, e il piano non lo dà per scontato. Lo misura C4: il Payment Link della beta mostra "€39 al lancio, €29 per sempre per i soci fondatori", con l'elenco qui sopra e senza audio.
- **≥3 soci fondatori**: Famiglia esce a €39 con questo contenuto. Il prezzo di €29 resta garantito ai soci.
- **1-2 soci**: le risposte aperte del sondaggio decidono cosa aggiungere, in quest'ordine di costo: momenti gialli rivisti, serie e memoria, audio con tetto. Il prezzo non scende sotto €29.
- **0 soci**: Famiglia non regge, e si applicano le regole PIVOT o STOP dello stress test.

Dopo il lancio pubblico, se nelle prime 4 settimane i checkout annuali a €39 sono meno della metà del tasso dei soci fondatori, si prova €29 come prezzo standard.

### 2.2 Favole gratuite e salvataggio

**Quante: 3 a settimana, finestra mobile di 7 giorni.**
- **Con 2** la soglia C1 (≥3 favole nella 2ª settimana) è irraggiungibile per chi usa il piano gratuito: il criterio principale diventa illeggibile.
- **Con 5** quasi nessuna famiglia in beta tocca il limite, e C4 perde la sua ragione d'essere: si chiede di pagare a chi non ha mai incontrato un confine.
- **Con 3** ogni famiglia che passa la soglia di attivazione incontra il paywall in quella stessa settimana. Il criterio di attivazione e il test di pagamento si leggono sulle stesse persone.
- **Costo.** Una famiglia gratuita costa al massimo circa 13 favole al mese, cioè circa €0,13 di AI. Con 300 famiglie attive (caso base: 1.000 registrati, 30% attivi) sono circa €39 al mese: dentro C8, ma il margine si consuma in fretta, ed è un altro motivo per non salire a 5.

**La quota si applica anche in beta**, dal primo giorno (passo 11 dell'Audit 2). Senza quota la beta misura l'uso di un prodotto illimitato e gratuito, che non esisterà mai.

**Correzione al testo.** La brand guide dice "Hai usato le 3 favole gratuite di questa settimana", mentre il server conta gli ultimi 7 giorni. Il messaggio diventa: "Hai usato le 3 favole gratuite di questi 7 giorni. La prossima si sblocca giovedì." Il giorno si calcola dalla favola più vecchia nella finestra. L'uscita "Torno la prossima settimana" diventa "Va bene, torno giovedì".

**Il salvataggio per tutti riduce le conversioni?** Il rischio esiste, ma è più piccolo del danno che farebbe chiuderlo.
- **Rischio.** I bambini amano riascoltare la stessa favola: una famiglia gratuita potrebbe rileggere quelle salvate invece di chiederne di nuove, e premere meno sulla quota.
- **Perché resta aperto.**
  - Il libro (C7) si compone con 6-8 favole salvate. Se il gratuito non salva, la seconda gamba vende solo agli abbonati, mentre il libro è pensato soprattutto per chi regala (nonni, zii).
  - La libreria è parte del rituale che deve far tornare la famiglia (C1).
  - Bloccare il salvataggio mette il paywall nel momento sbagliato: a fine favola, con il bambino addormentato.
- **Come si controlla.** Evento `story_reopened` in PostHog. Se dopo il lancio la conversione resta sotto il 2% (H4 basso) e le riletture superano il 40% delle sessioni gratuite, la prima leva da toccare è la quota (da 3 a 2, quando C1 non serve più a decidere), mai la libreria. La brand guide promette "Le favole che hai salvato restano tue anche nel piano gratuito", e la promessa resta.

**Il piano gratuito, quindi:** 3 favole ogni 7 giorni, durata fino a 6 minuti, tutti i temi quotidiani, i momenti difficili verdi, un profilo figlio con il nome, libreria senza limiti, modalità notte quando arriverà. Il libro si può comprare anche senza abbonamento.

### 2.3 Momenti difficili e temi spenti

**L'incoerenza.** L'Audit 1 e la brand guide usano i momenti difficili come leva d'acquisizione (messaggio B "Quando non sai come dirglielo", pagine SEO). L'Audit 2 li mette dietro il lucchetto e spegne i temi più delicati. La brand guide cita "mamma e papà in due case", che è un tema delicato, nel sottotitolo della pagina. L'Audit 2 chiama l'esperto dal giorno 1, lo stress test vieta consulenze prima del GO. Se il primo clic dalla landing B finisce su un lucchetto, il genitore torna su Gemini, che è gratis.

**La soluzione: tre livelli, una colonna `livello` in `story_themes`.**

| Livello | Criterio | Esempi | Gratuito | Famiglia | Marketing |
|---|---|---|---|---|---|
| **Verde** (sempre permessi) | Passaggi normali della crescita. Nessuna perdita, nessun danno, nessuna diagnosi, nessuna questione legale | Paura del buio, primo giorno al nido o a scuola, nuovo fratellino, gelosia, rabbia, litigio con un amico, dormire nel proprio letto, togliere il ciuccio o il pannolino, trasloco, visita dal pediatra o vaccino, genitore in viaggio per qualche giorno | Sì, dentro le 3 settimanali | Sì | Sì: landing B, pagina "momenti difficili", future pagine SEO |
| **Giallo** (dopo la revisione) | Perdita o cambiamento familiare reale, di cui il genitore deve aver già parlato | Separazione dei genitori, morte di un animale, lutto di un nonno, ricovero di un familiare, adozione, bullismo | No | Sì, solo dopo la revisione con il nome dell'esperto pubblicato | Solo dopo la revisione |
| **Rosso** (spenti) | Danno, pericolo o salute mentale; temi dove una favola generata può fare male o sostituire un aiuto professionale | Lista dell'Audit 2 (abuso, carcere, guerra, depressione, lutto di un genitore, coming out), più malattia grave del bambino, lutto di un fratello, violenza in famiglia, dipendenze, autolesionismo | No | No | Mai |

Dentro il rosso si fa una distinzione. **Abuso, violenza in famiglia e autolesionismo restano fuori per sempre**: lì la risposta giusta è indicare un aiuto, e una favola non basta. Gli altri temi rossi possono passare a giallo solo se l'esperto lo propone.

**"Scrivi tu" non deve aggirare le liste.** Prima della generazione, una chiamata breve a gpt-5-mini classifica il testo in verde, giallo o rosso (costo trascurabile, insieme alla moderazione del passo 9).
- **Verde**: si genera.
- **Giallo, prima della revisione**: "Per ora le favole su questo tema non sono pronte: vogliamo prima farle rivedere da uno psicologo dell'età evolutiva. Intanto, se ti serve, il pediatra è un buon punto di partenza." La frase dice un'intenzione, e quindi resta coerente con la regola 4 della brand guide (mai "rivisto da un esperto" senza un nome pubblico).
- **Rosso**: lo stesso messaggio, con l'avviso completo verso pediatra e psicologo.
- In tutti i casi il blocco non consuma la quota e viene registrato in PostHog come `theme_blocked` con il solo livello, senza il testo. Questo numero dice se la revisione dei gialli vale la spesa.

**Gli avvisi.**
1. **Sempre**, sotto ogni favola e pagina di un momento difficile, anche verde: l'avviso fisso della brand guide (regola 2).
2. **Prima di generare** un momento difficile: "Leggila prima tu, poi decidi se è quella giusta per stasera." Costa una riga di testo e protegge da una favola fuori bersaglio letta a voce senza averla vista prima.
3. **Nel prompt di sistema** (passo 15): le regole della brand guide §4.7 (niente morte mostrata, finale sicuro, adulto di riferimento presente) valgono per ogni favola, compresi i temi quotidiani.

**La revisione dell'esperto: quando e quanto.** Dopo il GO, prima del lancio pubblico. Oggetto: la lista dei gialli, le 3 frasi di avviso, il prompt di sistema, 10 favole di prova. Il preventivo va chiesto come pacchetto chiuso di 3-4 ore. È una stima da verificare, nell'ordine di qualche centinaio di euro. Con meno di 30 tentativi bloccati di livello giallo nella beta, la revisione può aspettare il lancio pubblico. Con di più, sale in testa allo Sprint 1.

**Correzioni alla brand guide.**
- Paywall, titolo "momento difficile": diventa "Questa situazione la scrivi tu con Famiglia" (per "Scrivi tu"). Il paywall sui momenti verdi sparisce.
- Pagina "momenti difficili": dal sottotitolo si toglie "mamma e papà in due case" e lo si sostituisce con un esempio verde ("la prima notte nel suo letto").
- §4, regola 3: la lista dei temi spenti diventa la colonna Rosso più la colonna Giallo di questa tabella, finché la revisione non c'è.

### 2.4 Minori: nome a OpenAI, consenso, testi privacy

Le valutazioni legali qui sotto vanno validate dal consulente privacy (§3, Dopo). Indicano la direzione e riducono il rischio da subito, ma non sostituiscono un parere.

**Il nome del bambino.**
- **Rischio.** Nome, età e situazione insieme formano un profilo di un minore. Con i temi gialli o con "Scrivi tu" possono toccare la salute o la vita familiare, cioè dati particolari (art. 9 GDPR). Nel passo 15 dell'Audit 2 il nome finisce nel prompt e quindi a un fornitore extra UE.
- **Soluzione: il segnaposto.** Il server manda a OpenAI il token `[[NOME]]` e il genere grammaticale scelto dal genitore (bambino, bambina, non specificato). Il nome vero viene inserito nel browser quando la favola si mostra. Nel database la favola si salva con il segnaposto e il riferimento al profilo figlio: cancellando il profilo, le favole restano senza nome. Il nome non transita mai nelle edge function, nei log o in PostHog.
- **Controllo.** Il server verifica che il testo contenga il segnaposto almeno una volta. Se manca, rigenera una volta. In beta si provano 20 generazioni: se il segnaposto si rompe più di 2 volte su 20, si usa un nome sentinella raro (per esempio "Zefiro") al posto del token, sostituito nello stesso modo.
- **"Scrivi tu".** Prima dell'invio, il browser sostituisce con il segnaposto i nomi dei profili figlio presenti nel testo. Sotto il campo compare: "Bastano poche parole. Non servono nomi né dettagli di salute."
- **Il testo libero non si conserva.** Si usa per generare e poi si scarta: nel database resta solo la favola. Va controllato che `story_generations` non lo salvi.

**Il consenso.**
- **Chi è l'utente.** Il servizio è rivolto ai genitori, e il bambino non ha un account. Le regole sul consenso del minore ai servizi online (art. 8 GDPR, in Italia 14 anni) e sull'accesso dei minori di 14 anni all'AI (L. 132/2025) riguardano il minore che usa il servizio: va quindi scritto e chiesto in modo esplicito che l'utente è un adulto. Da confermare con il consulente.
- **Registrazione**: casella obbligatoria "Ho almeno 18 anni e accetto Termini e Privacy". Il consenso marketing è separato e parte vuoto (passo 2f e 25).
- **Primo profilo figlio**: "Sono il genitore o chi ne fa le veci. Il nome resta in FavoLab: al servizio di AI non lo inviamo." La frase diventa vera grazie al segnaposto, e diventa anche un messaggio di fiducia usabile nel marketing.
- **Primo uso di "Scrivi tu"**: consenso esplicito, una volta sola: "Quello che scrivi viene inviato a OpenAI per creare la favola e poi non viene conservato." Copre l'art. 9 nel caso in cui il genitore scriva comunque qualcosa sulla salute.
- **Preordine del libro**: nome del bambino e indirizzo servono per stampare e spedire. Informativa breve nella landing, e il servizio di stampa va elencato tra i responsabili.

**I testi privacy e termini: minimo prima della beta, consulente dopo il GO.**

| Cosa | Quando | Costo |
|---|---|---|
| Privacy e Termini da un generatore (tipo iubenda), con titolare reale, responsabili (Supabase, OpenAI, Stripe, Google, PostHog, servizio di stampa), trasferimenti extra UE, conservazione, segnaposto del nome, nessun addestramento sui dati via API | Entra, entro il 20/10 | Decine di euro all'anno (stima), dentro C8 |
| DPA online già offerti da OpenAI, Supabase e Stripe: accettarli e archiviarli. Verificare la regione del progetto Supabase | Entra | €0 |
| Termini: utenti maggiorenni, favole per uso personale (stress test §3), dichiarazione che le favole sono scritte con l'AI, rinnovo e disdetta del socio fondatore | Entra | €0 |
| Dicitura "Scritta con l'aiuto dell'AI" su favola, PDF e libro. Gli obblighi di trasparenza dell'AI Act (art. 50) si applicano da agosto 2026: il consulente confermi se e come toccano FavoLab | Entra (la dicitura), Dopo (la verifica) | €0 |
| Consulente privacy: revisione dei testi, base giuridica dei temi, valutazione d'impatto se necessaria | Dopo il GO, prima del lancio pubblico | Una tantum, da preventivare |

Nessuna esenzione per la beta: 30-50 famiglie reali sono già trattamento di dati di minori a tutti gli effetti.

### 2.5 Altre incoerenze trovate

| # | Incoerenza | Decisione |
|---|---|---|
| 1 | Audit 2: lancio in 4 settimane. Stress test: con 5 ore a settimana servono 16-24 settimane | Vale lo stress test. Il lancio pubblico si pianifica dopo il GO, con l'ambito "Dopo" del §3 |
| 2 | Audit 2: privacy allo Sprint 3. Stress test: beta in settimana 2 | Il minimo legale si anticipa in Entra (§2.4) |
| 3 | Audit 2, passo 2e: `handle_new_user` smette di creare i profili figlio, ma il form di registrazione li chiede fino al passo 25 (Sprint 2) | Nello Sprint 0 si toglie solo la copia di `role`. L'inserimento dei figli resta finché il passo 25 non va in produzione, altrimenti in beta i nomi inseriti alla registrazione si perdono in silenzio |
| 4 | Audit 2: illustratore, esperto e consulente dal giorno 1. Stress test e brand guide: dopo le soglie | Dopo le soglie: illustratore con ≥15 preordini, esperto e consulente dopo il GO |
| 5 | Audit 2: "Scrivi tu" a pagamento. Audit 1: aperto a tutti | A pagamento (§2.1). Il gratuito riceve i momenti verdi |
| 6 | Audit 2, passo 17: suggerimenti di titoli protetti allo Sprint 1. Stress test: solo passi 10-11 prima della beta | La parte di autenticazione del passo 17 entra subito: è una funzione AI chiamabile senza account, lo stesso rischio di costo del passo 10 |
| 7 | Brand guide: "tuo figlio entra nella storia" vietata fino al rilascio. Il libro di Natale si chiama "Il libro di Mumi e [nome]" | Il nome nella favola (con segnaposto) entra prima della landing del libro, altrimenti le favole salvate da stampare non contengono il bambino |

---

## 3. Ambito del lancio

### Entra (entro il 7 novembre, circa 20-22 ore)

| # | Cosa | Passi Audit 2 | Criterio servito | Ore (stima) |
|---|---|---|---|---|
| E1 | Sicurezza: migrazione con la correzione del §2.5 n. 3, utente debug, file inutili, log della sessione, limite di spesa OpenAI | 1-7 | Prerequisito di qualunque famiglia esterna; C8 (limite di spesa) | 4 |
| E2 | Login obbligatorio e quota lato server (3 ogni 7 giorni, 5 al giorno per Famiglia), autenticazione sui suggerimenti di titoli | 10, 11, 17 (solo autenticazione) | C1 e C4 (il paywall esiste davvero); C8 (niente abusi) | 2 |
| E3 | Temi: tema letto dal DB, colonna `livello`, gialli e rossi spenti, classificatore su "Scrivi tu", messaggio di blocco, avvisi | 13, 39, più §2.3 | C2 e C5: una sola favola sbagliata letta a un bambino in beta brucia il passaparola nelle community, l'unico canale | 3 |
| E4 | Nome del bambino con segnaposto, chip del figlio con nome ed età, inserimento nel browser | 9, 14, 15, 27 e 29 in versione minima, più §2.4 | C3 (Mumi più il bambino contro la favola generica di Gemini); C7 (il libro porta il nome) | 2,5 |
| E5 | Salva per tutti; via i numeri inventati e "in un click" | 33 (solo Salva), 47 (solo TrustSection e home) | C1 (libreria e ritorno); C7 (favole da stampare); regole del §8 della brand guide | 0,5 |
| E6 | PostHog minimo, con `story_reopened` e `theme_blocked` | 45 | Misura di C1, C4, C5 | 1 |
| E7 | Privacy, Termini, DPA, caselle di consenso, dicitura AI | 46 e 25 in versione minima, più §2.4 | Prerequisito legale della beta | 2 |
| E8 | Payment Link socio fondatore €29/anno, attivazione a mano via SQL, link al portale clienti senza codice di Stripe per disdire | Stress test, settimana 2 | C4; "Disdici quando vuoi" resta vera | 0,5 |
| E9 | Landing del libro con mockup e Payment Link a €32, preventivi da 2 servizi di stampa | 55 (solo preordine) | C7 | 2 |
| E10 | Lavoro non tecnico: 5 post con UTM, test alla cieca con 10 genitori, sondaggio Sean Ellis (con una domanda su cosa manca a Famiglia), controllo TMview, lettura e decisione | Stress test §7 | C2, C3, C5; base per il §2.1 | 4 |
| | **Totale** | | | **circa 21,5** |

Se le ore non bastano, il primo taglio è il test Meta da €100 (C6). È l'unico criterio che non entra in nessuna regola GO, PIVOT o STOP, e lo scenario base già esclude la pubblicità.

### Non entra

| Cosa | Perché |
|---|---|
| Audio narrato dentro Famiglia a €39 senza tetto | Un uso serale costa €2,40 al mese contro €2,54 di ricavo netto dell'annuale (§2.1); indebolisce "con la tua voce" |
| Nome del bambino inviato a OpenAI | Sostituito dal segnaposto, in modo permanente |
| Temi rossi; abuso, violenza in famiglia e autolesionismo per sempre | §2.3 |
| Paywall sui momenti verdi | Bloccherebbe il primo clic del messaggio B, la leva d'acquisizione |
| Limiti sulla libreria gratuita | Rompono il libro (C7) e la promessa "restano tue" |
| Terzo piano (Cresci) e nomi Superpoteri o SuperGenitore | Brand guide, lessico fisso |
| Pubblicità a pagamento oltre il test da €100, salvo C6 ≤€1 | Stress test §2: il CAC non rientra in 12 mesi |
| Numeri di famiglie, testimonianze, "rivisto da un esperto" senza nome pubblico | Brand guide §8 |
| B2B2C come fonte di ricavo, altre lingue | Stress test §4: fuori dai vincoli di 5 ore e €5.000 |

### Dopo

| Cosa | Passi Audit 2 | Fattore scatenante |
|---|---|---|
| Stripe completo: webhook, annuale a €39, prova di 7 giorni, portale, disdetta alla cancellazione dell'account | 18-23 | GO (C1, C4, C5). Va fatto tutto insieme |
| Flusso in 3 tocchi completo, attesa onesta, modalità notte, header, pagina prezzi e paywall unico, prestazioni, SEO di base, pulizia del marchio | 25-38, 40-44, 47-48 | GO. È il lancio pubblico |
| Revisione dell'esperto e attivazione dei gialli per Famiglia | 53 | GO. Priorità più alta se `theme_blocked` gialli ≥30 in beta |
| Consulente privacy | 54 | GO, prima del lancio pubblico |
| Pagine SEO sui momenti verdi; sui gialli dopo la revisione | 60 | Lancio pubblico fatto |
| Streaming | 56 | Attesa mediana misurata sopra 40 secondi, oppure più del 10% di abbandoni durante l'attesa |
| Guest mode | 57 | Meno del 40% di chi tocca "Crea la tua prima favola" completa la registrazione |
| Audio con tetto (circa 10 al mese) o come aggiunta a pagamento | 59 | C4 tra 1 e 2 con l'audio tra le richieste, oppure ≥30% degli abbonati che lo chiede; costo per favola misurato |
| Pagina pubblica della storia condivisa | 58 | Lancio pubblico fatto |
| Memoria e serie di Mumi | 61 | Retention della 2ª settimana stabile ≥50% (H6) |
| Illustratore | 52 | ≥15 preordini (C7) |
| Libro con stampa via API | 55 | Più di circa 30 ordini |
| Deposito del marchio UIBM | | GO e TMview pulito |

## 4. Calendario (5 ore a settimana)

| Settimana | Lavoro | Uscita |
|---|---|---|
| 9-15 ottobre | E1, E6, inizio di E2; TMview | Sprint 0 in produzione |
| 16-22 ottobre | Fine di E2, E3, E4, E5, E7, E8; post nei gruppi | Le prime famiglie entrano il 20/10 (ultima data utile per C1: 24/10) |
| 23-29 ottobre | E9; test alla cieca; Meta se avanzano ore; Sean Ellis al 7º giorno | Landing del libro online |
| 30 ottobre - 7 novembre | Lettura delle metriche, decisione scritta | GO, PIVOT o STOP |

## 5. Da verificare

- Nel DB: elenco reale dei circa 90 temi (`select nome_tema, categoria, stato from story_themes`) e loro classificazione in verde, giallo e rosso. È un'ora di lavoro del fondatore, da fare dentro E3.
- Che `story_generations` non conservi il testo di "Scrivi tu".
- Tenuta del segnaposto `[[NOME]]` con gpt-5-mini e lo schema JSON (20 generazioni di prova).
- Regione del progetto Supabase e termini attuali dell'API di OpenAI su conservazione e addestramento.
- Con il consulente: ambito degli obblighi dell'AI Act (art. 50) e della L. 132/2025 per un servizio rivolto ai genitori; base giuridica dei temi che toccano la salute.
- Costo reale dell'audio per favola, prima di qualunque decisione sul punto "Audio" del Dopo.
