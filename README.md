# TPSIT · La mia pagina sotto Git

In questo esercizio metti la tua pagina HTML sotto Git e la fai crescere un commit alla volta.
Ogni `git push` è una consegna: si vede tutta la storia del tuo lavoro.

## 0. Prima volta: configura Git

Se non l'hai già fatto, nel terminale scrivi (con i tuoi dati):

```
git config --global user.name "Nome Cognome"
git config --global user.email "nome.cognome@marconirovereto.it"
git config --global init.defaultBranch main
```

## 1. Scarica il repository

Copia l'indirizzo del repository (pulsante verde **Code**) e scrivi:

```
git clone <indirizzo del repository>
cd <nome della cartella>
code .
```

## 2. Predici, poi verifica

Prima di eseguire ogni comando qui sotto, scrivi su un foglio **dove si trova `index.html`**
(working directory, staging area o repository) e **che cosa risponderà Git**. Poi eseguilo e confronta.

1. Modifica il titolo `<h1>` in `index.html` e salva. Poi: `git status`
2. `git add index.html`, poi `git status`
3. `git commit -m "feat: personalizza il titolo"`, poi `git status`
4. `git log --oneline`

Se la risposta di Git è diversa da quella che avevi previsto, scrivi accanto perché.

## 3. Fai crescere la pagina

Fai **almeno quattro commit**, uno per ogni passo. I messaggi seguono le
[Conventional Commits](https://www.conventionalcommits.org/it/v1.0.0/): `tipo: descrizione`, con il verbo
all'imperativo. I tipi che ti servono per ora:

| Tipo | Quando |
|---|---|
| `feat` | aggiungi qualcosa di nuovo (una sezione, un'immagine, una regola CSS) |
| `fix` | correggi un errore |
| `docs` | cambi solo la documentazione, per esempio questo README |
| `style` | sistemi rientri e spazi **senza cambiare quello che si vede** (non vuol dire «CSS»!) |

1. Sostituisci il contenuto di `index.html` con la tua pagina della «Consegna pagina HTML»,
   oppure completa lo scheletro che trovi. **Commit**, per esempio `feat: aggiungi la mia pagina`.
2. Crea `stile.css`, scrivi almeno una regola (per esempio il colore del titolo) e collegalo
   nella `<head>` con `<link rel="stylesheet" href="stile.css">`. **Commit**: `feat: aggiungi il foglio di stile`.
3. Cambia un paragrafo. Prima di `git add` scrivi `git diff`: che cosa ti mostra? **Commit**: scegli tu il tipo giusto.
4. Aggiungi un'immagine o un link, con i loro attributi. **Commit.**

Alla fine `git log --oneline` deve raccontare la storia della tua pagina.

Poi `git push`. Controlla su GitHub che ci siano tutti i commit.

## Se finisci prima

Modifica un file **senza** fare `git add`, poi scrivi `git restore <file>`. Che cosa è successo?
In quale delle tre aree hai lavorato?

## Se qualcosa non va

- **Il commit fallisce perché mancano nome ed email**: rifai il punto 0.
- **`git push` viene rifiutato**: scrivi prima `git pull`, poi di nuovo `git push`.
  Non usare mai `git push --force`.
