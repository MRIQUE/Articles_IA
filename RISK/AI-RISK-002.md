---
id: AI-RISK-002
type: risk
title: "MAESTRO : un cadre de modélisation des menaces pour l'IA agentique"
version: 1.0
status: draft
created: 2026-03-22
updated: 2026-03-22
---

# MAESTRO : modéliser les menaces spécifiques à l'IA agentique

## Résumé

Les systèmes d'IA agentique -- capables d'agir de manière autonome, d'apprendre et d'interagir entre eux -- posent des défis de sécurité que les cadres traditionnels de modélisation des menaces ne couvrent pas. En février 2025, la Cloud Security Alliance (CSA) a publié MAESTRO (Multi-Agent Environment, Security, Threat, Risk, and Outcome), un cadre conçu spécifiquement pour identifier, évaluer et atténuer les risques propres à ces architectures. Cet article en présente les principes, la structure et les apports.

## Les limites des cadres existants

Les cadres classiques de modélisation des menaces -- STRIDE, PASTA, LINDDUN, OCTAVE, Trike ou VAST -- ont été pensés pour des systèmes logiciels conventionnels. Ils couvrent efficacement les menaces génériques (usurpation d'identité, déni de service, violation de vie privée), mais échouent face aux spécificités de l'IA agentique. Trois catégories de lacunes ressortent. Premièrement, les menaces liées à l'autonomie : un agent peut prendre des décisions imprévisibles, ou voir ses objectifs détournés par un attaquant (goal misalignment). Deuxièmement, les menaces propres à l'apprentissage automatique : empoisonnement de données, attaques par évasion, extraction de modèle -- autant de vecteurs absents des cadres traditionnels. Troisièmement, les menaces liées aux interactions multi-agents : collusion entre agents, compétition destructrice, ou propagation d'un comportement corrompu dans un écosystème d'agents interconnectés.

## Une architecture de référence en sept couches

MAESTRO repose sur une architecture de référence à sept couches, chacune associée à un paysage de menaces spécifique. La couche 1 (modèles fondamentaux) couvre les attaques adversariales, le vol de modèle et l'empoisonnement des données d'entraînement. La couche 2 (opérations de données) traite de l'exfiltration, de la falsification et de la compromission des pipelines RAG. La couche 3 (frameworks agents) s'intéresse aux composants compromis, aux portes dérobées et aux attaques sur la chaîne d'approvisionnement logicielle. La couche 4 (infrastructure de déploiement) adresse les images conteneur malveillantes, les attaques d'orchestration et le détournement de ressources. La couche 5 (évaluation et observabilité) cible la manipulation des métriques et l'évasion des systèmes de détection. La couche 6 (sécurité et conformité), transversale, couvre l'empoisonnement des agents de sécurité eux-mêmes et les biais dans les décisions de protection. Enfin, la couche 7 (écosystème agents) traite des agents compromis, de l'usurpation d'identité entre agents et de la manipulation des registres de services.

## Les menaces inter-couches et les patterns architecturaux

Au-delà de chaque couche prise isolément, MAESTRO identifie des menaces qui traversent plusieurs niveaux. Un attaquant peut par exemple exploiter une vulnérabilité dans l'infrastructure (couche 4), injecter des données malveillantes dans le stockage (couche 2), et ainsi corrompre le modèle fondamental (couche 1) lors de sa prochaine mise à jour. Le cadre couvre également les principaux patterns architecturaux agentiques : agent unique (vulnérable à la manipulation d'objectifs), multi-agents (attaques sur les canaux de communication), agents conversationnels non contraints (injection de prompt), agents hiérarchiques (compromission d'un agent supérieur pour contrôler ses subordonnés), ou encore écosystèmes distribués (attaques Sybil par création de fausses identités). Chaque pattern est associé à des scénarios de menace et des stratégies d'atténuation ciblées.

## Les stratégies d'atténuation proposées

MAESTRO ne se limite pas à l'identification des menaces : il propose une démarche structurée en six étapes, de la décomposition du système selon les sept couches jusqu'à la mise en oeuvre et la surveillance continue. Les stratégies d'atténuation opèrent à trois niveaux. Au niveau de chaque couche, des contrôles spécifiques sont déployés (validation des entrées, chiffrement, contrôle d'accès). Au niveau inter-couches, le cadre préconise une défense en profondeur, une communication sécurisée entre les couches et une surveillance système globale. Enfin, au niveau spécifique à l'IA, MAESTRO recommande l'entraînement adversarial, la vérification formelle du comportement des agents, l'explicabilité des décisions (XAI) et le red teaming régulier.

## À retenir

MAESTRO comble un vide important dans la modélisation des menaces en proposant un cadre adapté à la complexité des systèmes d'IA agentique. Son approche par couches permet d'identifier des risques que les méthodes classiques ignorent, tandis que sa prise en compte des interactions multi-agents et des patterns architecturaux le rend opérationnel pour les équipes de sécurité. Alors que les agents IA se déploient massivement dans les environnements de production, disposer d'un cadre de menaces structuré et spécifique n'est plus optionnel -- c'est une nécessité.

## Sources

- Ken Huang, "[Agentic AI Threat Modeling Framework: MAESTRO](https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro)", Cloud Security Alliance, février 2025
- Ken Huang, "Generative AI Security: Theories and Practices", Springer, 2024
