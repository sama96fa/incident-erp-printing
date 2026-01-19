---
document: Post-mortem (mini)
auteur: Support IT
date: 2026-01-19
---

# Mini post-mortem — Panne impression ERP

## What happened
Lundi matin, l’impression depuis l’ERP ne fonctionnait plus pour ~25 utilisateurs. Incident détecté à 09h10, retour à la normale à 10h40. Un pilote d’impression incompatible a été introduit après une mise à jour Windows.

## Impact
- 25 utilisateurs impactés
- Impression ERP indisponible → traitement des documents ralenti

## Root cause
Pilote d’impression incompatible installé/activé suite à une mise à jour Windows.

## Detection
- Détection à 09h10 via signalements utilisateurs

## Response
- Analyse : lien avec mise à jour Windows
- Action : réinstaller/forcer un pilote compatible
- Validation : tests d’impression ERP OK

## Prevention
### Points positifs (2)
- Prise en charge rapide après détection
- Validation effectuée avant clôture (test d’impression OK)

### Axes d’amélioration (3)
- Mieux contrôler les mises à jour Windows sur les postes concernés
- Standardiser un pilote d’impression « référence »
- Documenter une procédure de dépannage impression ERP

### Actions correctives (4)
1. Vérification post-update Windows sur impression ERP
   - Responsable : Support Poste de travail
   - Délai : 2 semaines
2. Définir un pilote standard compatible pour les imprimantes concernées
   - Responsable : Équipe Infra/Print
   - Délai : 2 semaines
3. Créer/mettre à jour une KB « Impression ERP après update Windows »
   - Responsable : Support IT
   - Délai : 1 semaine
4. Ajouter un contrôle/tri des incidents d’impression (regroupement + escalade)
   - Responsable : Service Desk
   - Délai : 3 semaines
