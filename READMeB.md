# Le Survivant — histoire d'une thèse & analyseur d'opérations logico-discursives

Site en deux pages : le récit derrière la thèse de Jean Charconnet (1999, Paris VIII, préfacée par Jean-Blaise Grize), et un outil qui applique les 14 opérations de son tableau récapitulatif (Fig. 16) à l'analyse de textes — y compris, aujourd'hui, à la détection de dérives analogiques dans des sorties de LLM.

## Contenu

- **`index.html`** — la page d'accueil : l'histoire de la thèse, la préface de Grize, bilingue FR/EN.
- **`analyseur-grize.html`** — l'outil : repérage manuel et assisté par IA des opérations γ (faisceaux), ρ (domaines) et θ (désignation), suivi des classes-objets thème/phore, scoring de facteurs de risque d'hallucination, journal d'apprentissage.

Les deux fichiers sont autonomes (HTML/CSS/JS, sans dépendance de build) et se lient l'un à l'autre par chemin relatif — ils doivent rester dans le même dossier.

## Déployer sur GitHub Pages

1. Placez `index.html` et `analyseur-grize.html` à la racine du dépôt (ou dans un même sous-dossier, par exemple `/docs`).
2. Dans le dépôt GitHub : **Settings → Pages**.
3. Sous « Build and deployment », choisissez **Deploy from a branch**, puis sélectionnez la branche et le dossier où se trouvent les deux fichiers (`/root` ou `/docs`).
4. Enregistrez. GitHub Pages publie le site à une adresse du type `https://<votre-compte>.github.io/<nom-du-dépôt>/`.
5. La page d'accueil (`index.html`) s'ouvre par défaut ; le bouton « Ouvrir l'analyseur » mène à l'outil, qui propose un lien retour vers l'histoire.

Aucune étape de compilation n'est nécessaire — ce sont des fichiers statiques.

## Note sur l'outil

L'analyseur propose deux modes de repérage :
- **Détection par règles** — des motifs lexicaux locaux (comparatifs, reformulations, etc.), rapide mais à faible rappel sur des textes académiques réels, où les opérations sont rarement marquées par un mot-clé de surface.
- **Analyse par IA** — appelle un modèle avec les 14 opérations et des exemples authentiques du corpus de la thèse en contexte (few-shot), pour un jugement sémantique plutôt que lexical. Ce mode nécessite d'ouvrir le fichier comme artefact dans l'interface Claude.ai (pas comme simple fichier HTML local) pour que l'appel réseau fonctionne.

## Origine

D'après Jean-Blaise Grize, *Logique naturelle et communications*, PUF, 1996, et Jean Charconnet, *Analogie et logique naturelle*, Peter Lang, 2003 (préface de Grize) — issu de la thèse *Rhétorique de la découverte et de la vulgarisation scientifique*, Paris VIII, 1999.
