# Database delle attività sportive scolastiche

Esercitazione del quinto anno in **Microsoft Access**: un database per gestire le manifestazioni sportive tra scuole, cioè quali istituti partecipano, quali studenti si iscrivono a quali gare e quali professori accompagnano ogni manifestazione. Ho rielaborato il database partendo da un file di base fornito dal professore.

Scheda completa nel portfolio: <https://portfoliogigi.com/progetti/database-attivita-sportive/>

> **Dati e immagini fittizi.** Il file originale, usato a scuola, conteneva foto protette da copyright e dati di esempio con nomi e numeri di telefono. In questa versione pubblica nomi, telefoni e indirizzi sono inventati, le foto delle manifestazioni sono immagini di esempio con il nome dello sport e le immagini delle maschere sono state sostituite con grafiche neutre. Struttura, query e maschere sono quelle originali.

## Contenuto

| File | Descrizione |
|---|---|
| `Attivitasportive.accdb` | Database Access (formato 2007–2016) |

- **Cinque tabelle** collegate da **cinque relazioni uno a molti**: Istituti, Studenti, Professori, Manifestazioni e Partecipazione.
- **Una relazione molti a molti** tra studenti e manifestazioni, risolta con la tabella ponte *Partecipazione*.
- **Le tabelle scritte anche in SQL:** una query `CREATE TABLE` per ciascuna, con `PRIMARY KEY` e `FOREIGN KEY ... REFERENCES`.
- **Sei maschere:** una per ogni tabella e un **pannello di controllo** da cui raggiungerle.
- **Foto delle manifestazioni** salvate nel database, in un campo Oggetto OLE.
- Dati di prova: 5 istituti, 20 manifestazioni, 19 studenti e 19 professori.

## Come aprirlo

Serve **Microsoft Access** (2010 o successivo) su Windows. Scarica il file e aprilo; se compare l'avviso di sicurezza sul contenuto attivo, le tabelle, le query e le maschere funzionano anche senza abilitarlo. La maschera da cui partire è `Pannello_Controllo`.

## Limiti noti

- **Integrità referenziale:** le query SQL dichiarano le chiavi esterne, ma le relazioni del database non le applicano.
- **Professori e manifestazioni:** ogni professore può essere collegato a una sola manifestazione; una tabella ponte permetterebbe di assegnarlo a più gare.
- **Lunghezza dei campi:** con `char(25)` i nomi lunghi vengono tagliati, per esempio «Istituto Tecnico Tecnolog».
- **Foto dentro il database:** con le foto originali il file arrivava a circa 59 MB. Sarebbe meglio salvare le immagini in una cartella e nel database solo il percorso.

---

Autore: Luigi Lena · [portfoliogigi.com](https://portfoliogigi.com)
