# ⚖️ EU AI Act Compliance Checker

> Outil de pré-évaluation de la conformité d'un système IA selon le Règlement européen 2024/1689

**[🚀 Live Demo](https://TON-USERNAME.github.io/eu-ai-act-checker)**

---

## Aperçu

15 questions guidées pour classifier votre système IA selon l'EU AI Act et générer un rapport d'obligations personnalisé — sans compte, sans API, 100% client-side.

```
🔴 Interdit      → Pratiques totalement prohibées
🟠 Haut risque   → Obligations fortes avant mise sur le marché
🟡 Risque limité → Obligations de transparence
🟢 Risque minimal → Pas d'obligation spécifique EU AI Act
```

---

## Fonctionnalités

- **Questionnaire guidé** — 15 questions couvrant : domaine, nature du système, données, impact, surveillance, scoring, transparence, supervision humaine, documentation, biais, sécurité, gouvernance
- **Classification automatique** — algorithme de scoring pondéré selon les articles clés de l'EU AI Act
- **Rapport généré** — obligations applicables, calendrier de mise en conformité, actions recommandées
- **Glossaire intégré** — 20 définitions des termes clés du règlement
- **Base de cas d'usage** — exemples classifiés par niveau de risque
- **Export PDF** — via impression navigateur

---

## Structure du projet

```
eu-ai-act-checker/
├── checker.html              # Application principale (questionnaire + rapport)
├── classification_logic.js   # Données du rapport par niveau de risque + timeline
├── eu_ai_act_database.js     # Glossaire + base de cas d'usage
└── README.md
```

---

## Installation

**Pré-requis** : Live Server (VS Code) ou tout serveur HTTP local.

```bash
git clone https://github.com/TON-USERNAME/eu-ai-act-checker
cd eu-ai-act-checker
# Ouvrir checker.html avec Live Server dans VS Code
```

Ou directement sur **GitHub Pages** : aucune installation requise.

---

## L'algorithme de classification

Le système attribue des scores pondérés à chaque réponse selon 4 dimensions :

| Dimension | Exemples de facteurs |
|-----------|---------------------|
| **Interdit** | Surveillance biométrique RT, scoring social, manipulation subliminale |
| **Haut risque** | Domaine RH/santé/justice, impact sur droits fondamentaux, décision automatisée |
| **Risque limité** | Système conversationnel, contenu synthétique, marketing comportemental |
| **Risque minimal** | Usage interne, données anonymisées, supervision humaine forte |

La classification finale suit cette hiérarchie :
1. Score `interdit ≥ 5` → **Interdit**
2. Score `haut ≥ 6` → **Haut risque**
3. Score `limite ≥ 4` OU `haut ≥ 3` → **Risque limité**
4. Sinon → **Risque minimal**

> ⚠️ **Important** : Cet outil est une pré-évaluation indicative. Il ne remplace pas une analyse juridique professionnelle pour les décisions de conformité.

---

## Références légales

- [Règlement (UE) 2024/1689 — Texte officiel](https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX:32024R1689)
- [AI Office UE](https://digital-strategy.ec.europa.eu/en/policies/european-approach-artificial-intelligence)
- [CNIL — Guide EU AI Act](https://www.cnil.fr/fr/intelligence-artificielle)

---

## Stack technique

`HTML` · `CSS` · `Vanilla JavaScript` · `0 dépendance externe` · `100% client-side`

---

## Contribuer

Issues et Pull Requests bienvenus. Ce projet est open-source MIT.

```
feat: add new question on sector X
fix: scoring logic for biometric systems
docs: update glossary with Art. 50 details
```

---

*Projet personnel — outil d'aide à la compréhension de l'EU AI Act, pas un conseil juridique.*
