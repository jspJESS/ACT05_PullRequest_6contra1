# ACT05 · Pull request: sis alumnes contra una

**Durada: 60 minuts · Sis torns individuals**

## Objectiu

Practicar el flux de col·laboració amb Git i GitHub: crear una branca, guardar i pujar un canvi, obrir una pull request, respondre a una revisió i integrar el canvi a `main`.

## Abans de començar

El docent us donarà l'URL d'un repositori compartit. Cada alumne ha de tenir permís d'escriptura i haver acceptat la invitació abans de la sessió. Cloneu el repositori a l'ordinador abans de començar.

El docent assignarà un torn i una branca a cadascú: `millora-01`, `millora-02`, `millora-03`, `millora-04`, `millora-05` o `millora-06`. Només treballa una persona cada vegada. La resta observa la revisió.

## 1. Clona el repositori — abans de la sessió

Substitueix `<URL_DEL_REPOSITORI>` per l'adreça que t'ha donat el docent:

```bash
git clone <URL_DEL_REPOSITORI>
cd ACT05_PullRequest_6contra1
git status
```

Comprova que ets a la branca `main` i que l'arbre de treball està net. No facis canvis directament a `main`.

## 2. Quan comenci el teu torn: actualitza i crea una branca — 1 minut

Abans de començar, incorpora els canvis que el docent hagi integrat al torn anterior i crea la branca que t'ha assignat:

```bash
git switch main
git pull origin main
git switch -c millora-01
```

Fes servir el nom de branca assignat. Per exemple, el segon alumne farà servir `millora-02`.

## 3. Proposa una millora — 2 minuts

Edita `idees.md` i afegeix al final una proposta concreta per millorar el cartell de la Fira DAW. Explica també per què seria útil. No esborris les propostes anteriors.

Revisa, prepara i desa el canvi:

```bash
git status
git diff
git add idees.md
git diff --staged
git commit -m "Proposa una millora per al cartell"
git push -u origin millora-01
```

Al comandament `git push`, fes servir el nom de branca que t'han assignat.

## 4. Obre una pull request — 1 minut

A GitHub, obre el repositori compartit i crea una pull request amb aquests valors:

- **Base:** `main`
- **Compare:** la teva branca (`millora-01`, `millora-02`, etc.)
- **Títol:** `Millora del cartell de la Fira DAW`
- **Descripció:** resumeix què proposes i per què.

Espera la revisió del docent. No integris tu mateix/a la pull request.

## 5. Respon a la revisió — 2 minuts

El docent et deixarà un comentari o una pregunta. Edita `idees.md` per respondre-hi i desa l'ajust en un altre commit:

```bash
git add idees.md
git commit -m "Aclareix la proposta del cartell"
git push
```

La pull request s'actualitzarà amb el nou commit. El docent revisarà el canvi i l'integrarà a `main`.

## 6. Observa els torns següents

Després que el docent integri la pull request, la persona següent actualitza `main` amb `git pull origin main` abans de crear la seva branca. Així treballa sobre l'última versió integrada.

## Tancament — 8 minuts

Comenteu entre tots:

1. Què mostra una pull request abans d'integrar-la?
2. Què ha canviat a la pull request després del segon `push`?
3. Quina diferència hi ha entre `commit` i `push`?
4. Què ha fet que la proposta aparegui a `main`?

## Temps de la sessió

- Presentació i recordatori del flux: 5 minuts.
- Sis torns de 7 minuts: 42 minuts.
- Posada en comú: 8 minuts.
- Marge per a incidències: 5 minuts.

Perquè càpiga en una hora, tothom ha d'haver clonat el repositori i acceptat la invitació abans de la sessió.

## Comandaments de la pràctica

- `git clone`: descarrega el repositori.
- `git switch main`: canvia a la branca principal.
- `git pull`: actualitza la branca local amb els canvis de GitHub.
- `git switch -c`: crea una branca i hi canvia.
- `git status`: mostra l'estat dels fitxers.
- `git diff`: mostra els canvis que encara no estan preparats.
- `git add`: prepara els fitxers per al commit.
- `git diff --staged`: mostra els canvis preparats.
- `git commit`: desa els canvis a l'historial.
- `git push`: puja els commits a GitHub.
