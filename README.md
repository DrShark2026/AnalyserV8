# Le Survivant — histoire d'une thèse & analyseur d'opérations logico-discursives

Site en deux pages : le récit derrière la thèse de Jean Charconnet (1999, Paris VIII, préfacée par Jean-Blaise Grize), et un outil qui applique les 14 opérations de son tableau récapitulatif (Fig. 16) à l'analyse de textes — y compris, aujourd'hui, à la détection de dérives analogiques dans des sorties de LLM.

## Contenu

- **`index.html`** — la page d'accueil : l'histoire de la thèse, la préface de Grize, bilingue FR/EN.
- **`analyseur-grize.html`** — l'outil : repérage manuel et assisté par IA des opérations γ (faisceaux), ρ (domaines) et θ (désignation), suivi des classes-objets thème/phore, scoring de facteurs de risque d'hallucination, journal d'apprentissage.
- **`these-charconnet-1999.pdf`** — le texte intégral de la thèse (383 pages), mise en page d'origine.
- **`couverture-livre.jpg`**, **`jean-mathias-1999.jpg`**, **`famille-2022.jpg`** — photos illustrant le récit.
- **`.nojekyll`** — désactive le moteur Jekyll de GitHub Pages, pour que les fichiers soient servis tels quels.

Tous les fichiers sont autonomes (HTML/CSS/JS, sans dépendance de build) et se lient entre eux par chemin relatif — ils doivent rester dans le même dossier.

## Déployer sur GitHub Pages

1. Placez tous les fichiers ci-dessus à la racine du dépôt (ou dans un même sous-dossier, par exemple `/docs`).
2. Dans le dépôt GitHub : **Settings → Pages**.
3. Sous « Build and deployment », choisissez **Deploy from a branch**, puis sélectionnez la branche et le dossier où se trouvent les fichiers (`/root` ou `/docs`).
4. Enregistrez. GitHub Pages publie le site à une adresse du type `https://<votre-compte>.github.io/<nom-du-dépôt>/`.
5. La page d'accueil (`index.html`) s'ouvre par défaut ; le bouton « Ouvrir l'analyseur » mène à l'outil, qui propose un lien retour vers l'histoire.

Aucune étape de compilation n'est nécessaire — ce sont des fichiers statiques.

## Note sur l'outil

L'analyseur propose deux modes de repérage :
- **Détection par règles** — des motifs lexicaux locaux (comparatifs, reformulations, etc.), rapide mais à faible rappel sur des textes académiques réels, où les opérations sont rarement marquées par un mot-clé de surface.
- **Analyse par IA** — appelle un modèle avec les 14 opérations et des exemples authentiques du corpus de la thèse en contexte (few-shot), pour un jugement sémantique plutôt que lexical. Ce mode nécessite d'ouvrir le fichier comme artefact dans l'interface Claude.ai (pas comme simple fichier HTML local) pour que l'appel réseau fonctionne.

## Origine

D'après Jean-Blaise Grize, *Logique naturelle et communications*, PUF, 1996, et Jean Charconnet, *Analogie et logique naturelle*, Peter Lang, 2003 (préface de Grize) — issu de la thèse *Rhétorique de la découverte et de la vulgarisation scientifique*, Paris VIII, 1999.

---

# The Survivor — the story of a thesis & logico-discursive operations analyser

*(English version)*

A two-page site: the story behind Jean Charconnet's thesis (1999, Paris VIII, prefaced by Jean-Blaise Grize), and a tool that applies the 14 operations from its summary table (Fig. 16) to text analysis — including, today, the detection of analogical drift in LLM output.

## Contents

- **`index.html`** — the homepage: the story of the thesis, Grize's preface, bilingual FR/EN.
- **`analyseur-grize.html`** — the tool: manual and AI-assisted tagging of the γ (bundle), ρ (domain), and θ (designation) operations, theme/phore object-class tracking, hallucination-risk scoring, learning journal.
- **`these-charconnet-1999.pdf`** — the full text of the thesis (383 pages), original layout.
- **`couverture-livre.jpg`**, **`jean-mathias-1999.jpg`**, **`famille-2022.jpg`** — photos illustrating the story.
- **`.nojekyll`** — disables GitHub Pages' Jekyll engine, so files are served as-is.

All files are self-contained (HTML/CSS/JS, no build step) and link to each other by relative path — they must stay in the same folder.

## Deploying on GitHub Pages

1. Place all the files above at the repository root (or in the same subfolder, e.g. `/docs`).
2. In the GitHub repo: **Settings → Pages**.
3. Under "Build and deployment", choose **Deploy from a branch**, then select the branch and folder where the files live (`/root` or `/docs`).
4. Save. GitHub Pages publishes the site at an address like `https://<your-account>.github.io/<repo-name>/`.
5. The homepage (`index.html`) opens by default; the "Open the analyser" button leads to the tool, which offers a link back to the story.

No build step is needed — these are static files.

## Note on the tool

The analyser offers two tagging modes:
- **Rule-based detection** — local lexical patterns (comparatives, rewordings, etc.), fast but low-recall on real academic text, where operations are rarely marked by a surface keyword.
- **AI analysis** — calls a model with the 14 operations and authentic examples from the thesis corpus in context (few-shot), for a semantic rather than lexical judgment. This mode requires opening the file as an artifact inside the Claude.ai interface (not as a plain local HTML file) for the network call to work.

## Origin

After Jean-Blaise Grize, *Logique naturelle et communications*, PUF, 1996, and Jean Charconnet, *Analogie et logique naturelle*, Peter Lang, 2003 (preface by Grize) — drawn from the thesis *Rhétorique de la découverte et de la vulgarisation scientifique*, Paris VIII, 1999.
