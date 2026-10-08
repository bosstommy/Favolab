# FavoLab · Brand guide v1

8 ottobre 2026. Base: decisione strategica del passo 1 (GO condizionato su "freemium annuale + libro di Mumi", stress test), Audit 1, Audit 2. Ogni promessa è verificata sul codice di `bedtime-tales-for-kids` (`main`, commit `90e4472`), dove oggi nessun passo dell'Audit 2 è ancora applicato. Le promesse valgono solo nello stato indicato al §8.

---

## 1. Chi serviamo

**Chi paga: il genitore stanco della sera.**
- Mamma o papà di un bambino tra 3 e 7 anni (il prodotto copre 2-10, il messaggio parla a 3-7). Italia, smartphone, ore 20:30-21:30.
- Legge già le favole o vorrebbe farlo. È stanco, ha poco tempo e poca voglia di inventare.
- Due momenti d'acquisto:
  - **la sera normale**: "non ho idee e non ho energie" (porta l'uso e la retention);
  - **il giorno difficile**: un litigio all'asilo, un fratellino in arrivo, la paura del buio. "Non so come parlargliene" (porta l'acquisizione e l'abbonamento).
- Dove sta: gruppi e community di genitori, WhatsApp di classe, pediatra. Unico canale gratuito oggi.
- Cosa teme: schermi, contenuti AI strani, dati del figlio in giro, abbonamenti che non si disdicono.

**Chi usa: il bambino che ascolta.**
- Non tocca il telefono e non vede l'app. Ascolta la voce del genitore.
- Vuole: Mumi, gli amici del bosco, ritrovarsi nella storia, un finale che lo calma.
- Conseguenza di brand: tutto ciò che vede il genitore parla al genitore; tutto ciò che sente il bambino è la favola. Mumi vive solo nella favola e nelle illustrazioni.

**Chi regala (seconda gamba, libro):** nonni e zii, a Natale e ai compleanni. Si raggiungono tramite il genitore.

**Fuori target per ora:** scuole, pedagogisti come clienti, bambini che usano l'app da soli, mercati esteri.

## 2. Promessa

**Promessa unica (versione di lancio):**
> **La favola giusta per la giornata di tuo figlio, pronta in meno di un minuto, da leggere con la tua voce.**

Si regge su tre fatti: storia nuova e su misura per età e tema (vero oggi); attesa reale 20-40 secondi (da misurare in beta, §8); la legge il genitore, nessuno schermo davanti al bambino (vero per come funziona il prodotto).

**3 alternative da testare** (stesso post in community con UTM diversi, oppure 3 varianti della landing nel test Meta da €100; metrica: click e registrazioni per variante, minimo 100 visite ciascuna):

| | Leva | Frase | Vince se |
|---|---|---|---|
| A | Rituale | Ogni sera una favola nuova di Mumi, su com'è andata oggi. | porta più registrati che tornano nella 2ª settimana |
| B | Parole difficili | Quando non sai come dirglielo, Mumi trova le parole con te. | porta più click sul paywall dei momenti difficili |
| C | Stanchezza | Sei stanco? Tre tocchi e la favola di stasera è pronta. | porta il tasso di registrazione più alto |

La promessa unica resta finché un'alternativa non supera del 30% la sua conversione.

## 3. Architettura: FavoLab e Mumi

| | FavoLab | Mumi |
|---|---|---|
| Ruolo | Il marchio, la casa editrice. Garantisce, incassa, protegge | Il personaggio. Vive nelle favole, nelle illustrazioni, sul libro |
| Parla a | Genitore | Bambino (attraverso la voce del genitore) |
| Dove | Header, prezzi, paywall, email, privacy, termini, ricevute | Titoli delle storie, illustrazioni, copertina del libro, attesa ("Mumi sta scrivendo") |
| Regola | Firma ogni promessa commerciale | **Mumi non vende mai.** Niente Mumi che chiede soldi, che si dispiace se disdici, che spinge a comprare |

Formula di marca: **FavoLab · le favole di Mumi**. Il libro si chiama "Il libro di Mumi e [nome]", edito da FavoLab.

**Il nome FavoLab comunica calore da buonanotte?** In parte.
- A favore: "Favo" richiama subito "favola"; è breve, unico, già sul logo e nel codice. "Favo" è anche l'alveare: un appiglio caldo (miele, Api Gemelle) già coerente con la palette.
- Contro: "Lab" evoca laboratorio, esperimento, tecnologia. Alle 21 il genitore cerca una coperta, e "Lab" rischia di suonare come "favole fatte in provetta", proprio il dubbio sull'AI che vogliamo sciogliere.
- **Decisione:** si tiene FavoLab come marchio ombrello (domini, Stripe, legale, nessun costo di cambio) e si affida il calore a Mumi in prima linea: titolo della home "Le favole di Mumi", FavoLab nel logo e nella firma. In beta si testa un headline con "FavoLab" contro uno con "Mumi"; se Mumi vince nettamente, il dominio resta e cambia solo la gerarchia visiva.
- **Nome del personaggio:** "Mumi" confermato dal fondatore l'8 ottobre 2026. Nel disegno si evita ogni somiglianza con i Moomin (in italiano "Mumin").

## 4. Tono di voce

**Chi parla:** un'amica che ha letto tanti libri sull'infanzia e ne parla semplice. Voce bassa da sera: frasi corte, verbi concreti, seconda persona singolare (tu), zero urgenza.

Quattro regole:
1. **Concreto prima di bello.** Si dice cosa succede ("tre tocchi, venti secondi"), poi l'emozione.
2. **Il genitore è bravo.** Si aiuta, mai si corregge né si colpevolizza.
3. **L'AI si dice e si dosa.** La si nomina con onestà dove serve (come nascono le favole, privacy), mai come vanto.
4. **Nessuna urgenza.** Niente countdown, maiuscole, "ultima occasione".

| Sì | No |
|---|---|
| Com'è andata oggi? | Seleziona la categoria tematica |
| Mumi sta scrivendo la vostra favola. Di solito ci vogliono 20-40 secondi. | In pochi secondi la magia è pronta! ✨ |
| Hai usato le 3 favole gratuite di questa settimana. | Limite raggiunto! Sblocca ORA i Super Poteri 🚀 |
| Leggila con la tua voce: è quella che conta. | La nostra AI rivoluzionaria crea storie uniche |
| Disdici quando vuoi, in due clic. | Offerta valida solo oggi |
| Una favola per parlarne insieme. | Una favola che risolve la paura del buio |
| Tuo figlio entra nella storia, accanto a Mumi. | Il tuo bambino è il protagonista! (oggi falso) |

Lessico fisso: *favola* (mai "contenuto", "output"); *Famiglia* per il piano a pagamento (mai Superpoteri, Cresci, SuperGenitore); *momenti difficili*; *Racconta* per il bottone. Grafia sempre **FavoLab**. Emoji: al massimo una, solo nei messaggi di servizio.

**Regole per i temi sensibili** (separazione, lutto, malattia, nuovo fratellino, adozione, paure, rabbia):
1. **La favola accompagna.** Mai promettere una cura: mai "risolve", "guarisce", "terapeutica". Si dice "per parlarne insieme", "per trovare le parole".
2. **Avviso fisso** su ogni pagina e storia di momento difficile: "Le favole aiutano a parlare. Se il disagio dura o ti preoccupa, parlane con il pediatra o con uno psicologo dell'età evolutiva."
3. **Temi spenti finché un esperto non li rivede** (Audit 2, passo 39): abuso, carcere, guerra, depressione, lutto di un genitore, coming out. Non si nominano nel marketing.
4. **Mai "rivisto da un esperto"** finché il nome dell'esperto non è pubblico su "Come nascono le favole" (passo 53).
5. **Linguaggio delle situazioni:** descrittivo e senza etichette ("quando mamma e papà vivono in due case", non "divorzio traumatico"; "quando arriva un fratellino", non "gelosia patologica").
6. **Nessuna storia reale di bambini** nel marketing senza consenso scritto del genitore; nessun dato del tema nelle analytics.
7. **Nelle favole:** niente morte mostrata, niente paura senza rifugio, finale sempre sicuro, adulto di riferimento presente (mamma o papà di Mumi, Gufo Gaia).

## 5. Mappa dei concorrenti

Due assi: **storia generica ↔ su misura per la giornata del bambino**; **schermo o voce sintetica ↔ voce del genitore**.

| Concorrente | Su misura | Voce | Lingua e personaggio | Prezzo |
|---|---|---|---|---|
| Gemini Storybook, ChatGPT | Sì, se scrivi un buon prompt | Schermo, audio sintetico | Generico, nessun personaggio fisso | Gratis |
| fiabe.ai, Oscar Stories, Lume, Nara | Sì (nome, parametri) | Spesso audio e immagini sullo schermo | Inglese o tradotto, protagonista sempre diverso | Crediti o abbonamento |
| Yoto, audiolibri, podcast di favole | No | Voce registrata, nessuno schermo | Catalogo fisso | Hardware + carte, abbonamenti |
| Libri illustrati, "Favole al telefono" | No | Voce del genitore | Personaggi amati | €10-20 una tantum |
| Libri personalizzati (Wonderbly) | Solo il nome | Voce del genitore | Storia fissa | €35-45, regalo |

**Il vuoto che occupiamo:** la favola **su misura per la giornata di oggi**, **in italiano**, **letta dal genitore**, con **un personaggio fisso che il bambino ritrova ogni sera** e un percorso sui momenti difficili. I gratuiti fanno la storia singola meglio di noi: si vince sul rituale (Mumi, libreria, 3 tocchi, modalità notte), sulla fiducia e sull'oggetto fisico.

## 6. Brief visivo e bibbia di Mumi

**Base visiva (dal codice, da tenere):**
- Fondo crema `#FFFCF8`, card `#FFF8F0`; miele `#FFD9A0` (CTA), beige dorato `#FFE3BA`, salvia `#C2E1C2`; testo marrone caldo `#3B322B`.
- Notte (lettura): fondo `#1d1915`, testo `#f3e9dc`, nessuna animazione. Da correggere: il tema scuro attuale in `src/index.css` usa i blu di default di shadcn, fuori palette.
- Font: Nunito per titoli e bottoni, Lato per il testo. Storia in corpo grande (18-24 px).
- Fotografie: nessuna foto di bambini. Solo illustrazioni.
- Interfaccia: angoli morbidi, poco testo, un'azione per schermata.

**Brief per l'illustratore** (si commissiona solo dopo il GO del 7 novembre o con ≥15 preordini del libro; budget €1.500-3.000; **cessione scritta dei diritti economici** su personaggi e scene, uso anche commerciale e per merchandising).

*Mumi.* Cucciola di volpe rossa, circa 5 anni "umani" (femmina, confermato: va fissato ovunque, prompt e testi compresi). Antropomorfa leggera: cammina su due zampe, nessun vestito tranne la **sciarpa verde salvia**, suo segno distintivo. Testa grande (1:2,5 sul corpo), occhi scuri grandi e vivi, muso corto, pancia e punta della coda crema. Curiosa, sensibile, a volte impulsiva; sbaglia e ci riprova. Vive in una tana sotto le radici di una quercia, con una lampada calda e un lettino di foglie.

*Il cast* (qualità dal prompt attuale, unificate nel cast unico del passo 8):

| Personaggio | Qualità nelle storie | Indizio visivo |
|---|---|---|
| Mamma di Mumi | calore, sicurezza | volpe adulta, grembiule o scialle |
| Papà di Mumi | forza, avventura | volpe adulta più alta, zaino |
| Lupo Leo | coraggio, rabbia gestita | grosso e goffo, sguardo buono |
| Riccio Rocco | timidezza, paura del giudizio | piccolo, si chiude a palla |
| Tartaruga Tea | calma, pazienza | occhiali, guscio con disegni |
| Cavallo Carlo | energia, movimento | criniera al vento, sempre in corsa |
| Api Gemelle | squadra, solidarietà | due api quasi uguali, un dettaglio diverso |
| Gufo Gaia | saggezza, memoria | occhiali tondi, libri nella cavità della quercia |
| Pulcino Pino | primo distacco, fiducia | piccolissimo, guscio ancora in testa |

*Stile.* Gouache o acquerello digitale, tratto morbido, luce di lampada e di tramonto, palette calda con verdi salvia. Pochi dettagli sullo sfondo. Espressioni leggibili da un bambino di 3 anni. Da evitare: estetica 3D tipo Pixar, somiglianze con volpi note (Nick di Zootropolis, Mr. Fox, Tails), forme tonde bianche che ricordino i Moomin, scritte dentro le immagini.

*Consegne.*
- Model sheet per ogni personaggio: 3 viste, 6 espressioni (felice, triste, arrabbiata, impaurita, sorpresa, assonnata).
- 20 scene base riutilizzabili, in orizzontale 3:2 e in verticale per la copertina: tana fuori e dentro; Mumi a letto; cena in famiglia; radura; ruscello; sentiero nelle 4 stagioni (4 tavole); quercia di Gaia di notte; stagno di Tea; prato di Carlo; alveare; scuola del bosco; Mumi arrabbiata; Mumi triste abbracciata; Mumi con un amico visto di spalle (per "il bambino" nel libro); festa nel bosco; buonanotte finale.
- File sorgente a livelli, 300 dpi, profilo per la stampa. Una OG image 1200×630 e un'icona di Mumi quadrata.

## 7. Messaggi per le tre situazioni

**Homepage** (prima schermata di un telefono 390×844)
- Titolo: **Le favole di Mumi, su misura per la giornata di tuo figlio.**
- Sottotitolo: Scegli per chi, racconta com'è andata oggi: in meno di un minuto hai una favola nuova da leggere con la tua voce.
- CTA: **Crea la favola di stasera**
- Tre passi: Per chi? · Com'è andata oggi? · Racconta.
- Riga di fiducia: 3 favole gratis ogni settimana · Senza pubblicità · Disdici quando vuoi.

**Paywall** (quarta favola della settimana, oppure tocco su un momento difficile o su "Scrivi tu")
- Titolo, quota: Hai usato le 3 favole gratuite di questa settimana.
- Titolo, momento difficile: I momenti difficili sono nel piano Famiglia.
- Corpo: Con Famiglia hai favole senza limiti, i momenti difficili, la situazione scritta da te e un profilo per ogni figlio. Le favole che hai salvato restano tue anche nel piano gratuito.
- Prezzo: **€39 all'anno** (circa €3,25 al mese) · oppure €4,99 al mese.
- CTA: **Prova 7 giorni gratis** · sotto: Ti avvisiamo prima del rinnovo. Disdici in due clic dall'area personale.
- Uscita: Torno la prossima settimana (sempre visibile, mai nascosta).
- Variante beta (stress test, settimana 2): "Diventa socio fondatore: €29 all'anno, per sempre."

**Pagina "momenti difficili"**
- Titolo: **Quando non sai come dirglielo.**
- Sottotitolo: Il primo giorno al nido, un fratellino in arrivo, la paura del buio, mamma e papà in due case. Racconti a FavoLab cosa sta succedendo e Mumi lo vive in una favola, con le parole giuste per la sua età.
- Come funziona: scegli la situazione o scrivila con parole tue · leggete la favola insieme · in fondo trovi tre domande per parlarne, nel riquadro "Per te, genitore".
- Avviso fisso (§4, regola 2).
- CTA: **Crea una favola per questo momento** (porta al paywall per il piano gratuito).
- Vietato qui: elenco dei temi spenti, numeri di famiglie aiutate, citazioni di esperti senza nome.

## 8. Ogni promessa contro il prodotto reale

| Promessa | Oggi su `main` | Diventa vera con (Audit 2) | Regola |
|---|---|---|---|
| Su misura per età e tema | Vera (fasce d'età, ~90 temi) | | Usabile |
| Da leggere con la tua voce, nessuno schermo per il bambino | Vera: il prodotto è testo letto dal genitore | | Usabile |
| Senza pubblicità | Vera | | Usabile |
| Meno di un minuto / 20-40 secondi | Non misurata; la home dice "in un click", HowItWorks "in pochi secondi" | Passo 32 + misura in PostHog in beta | Usare solo dopo la misura; togliere subito "un click" e "pochi secondi" |
| Tre tocchi | Falsa (circa 11 tocchi più la conferma email) | Passi 25-30 | Vietata fino al rilascio dello Sprint 2 |
| Tuo figlio entra nella storia | Falsa; OurStory dice "ogni bambino protagonista" | Passi 15 e 29 | Vietata fino al rilascio; poi solo "accanto a Mumi" |
| 3 favole gratis a settimana, salvate | Limite solo nel browser; "Salva" disabilitato per il piano gratuito | Passi 11, 31, 33 | Vietata fino al rilascio |
| Prova 7 giorni, €39/anno, disdici in due clic | Nessun webhook, `isAnnual` ignorato, nessun portale | Passi 18-22 | Vietata finché il collaudo del passo 49 non passa |
| Momenti difficili curati da un esperto | Nessun esperto coinvolto; temi delicati attivi | Passi 39 e 53 | Vietata; dire solo "scritti con cura" |
| I dati di tuo figlio sono al sicuro | Falsa: RLS che permettono di cambiare piano e ruolo | Sprint 0 (passi 1-7) e 46 | Vietata fino allo Sprint 0 in produzione e alla privacy corretta |
| Modalità notte | Assente | Passo 34 | Vietata fino al rilascio |
| Mumi e i suoi amici, sempre gli stessi | Cast diverso tra le due funzioni (Riccio Rocco e Pulcino Pino) | Passo 8 | Usabile dopo il passo 8 |
| Audio narrato | Assente, fuori dal lancio | Dopo il lancio (passo 59) | Vietata, anche nel paywall |
| Il libro di Mumi e [nome] | Assente | Preordine manuale (passo 55) | Solo come "preordine", con data di consegna e rimborso se non si stampa |
| Numeri di famiglie e storie ("500+") | Inventati in `TrustSection.tsx` | Passo 47 li elimina | Vietati finché non sono dati reali |

**Conseguenza per la beta (fine ottobre):** i messaggi del §7 si usano solo nelle parti già vere. Per i 30-50 genitori della beta la home dice "Crea la favola di stasera" e "una favola nuova su misura per età e giornata"; il paywall è il Payment Link da socio fondatore con attivazione manuale, senza prova gratuita automatica.
