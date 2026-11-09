# Registre des risques — Attrape les pommes

Échelles : P et I de 1 à 3. Criticité = P × I
(1-2 faible, 3-4 moyenne, 6-9 élevée). Revu à chaque sprint planning.

## Synthèse (de la criticité la plus haute à la plus basse)

| ID | Risque | Criticité | Responsable |
|----|--------|-----------|-------------|
| R1 | Collisions mal détectées | 6 (élevée) | Amine |
| R2 | Retard des fonctionnalités Unity | 6 (élevée) | Amine |
| R4 | Retard causé par une absence | 4 (moyenne) | Amine |
| R5 | Fonctionnalités marquées terminées trop tôt | 4 (moyenne) | Amine |
| R3 | Compteur mal affiché | 3 (moyenne) | Amine |
| R6 | Son de ramassage trop fort | 1 (faible) | Amine |

## R1 — Collisions mal détectées

- **Risque :** Parce que BF-01 déplace le panier pendant que BF-06 fait tomber les pommes, il est possible qu'une collision ne soit pas détectée, ce qui empêcherait BF-05 de compter certaines pommes.
- **BF touchés :** BF-01, BF-05, BF-06
- **Catégorie :** Technique
- **P :** 2 (les déplacements, les pommes et le compteur doivent fonctionner ensemble) · **I :** 3 (BF-05 est Essentiel) · **Criticité :** 6 (élevée)
- **Stratégie :** Réduire
- **Mitigation :** Faire 10 tests où une pomme touche le panier et noter le résultat dans l'issue BF-05. Le compteur doit augmenter pour les 10 tests.
- **Déclencheur :** Au moins une des 10 pommes touchant le panier n'est pas comptée.
- **Contingence :** Vérifier les Collider2D et le Rigidbody2D, corriger la détection des contacts, puis refaire les 10 tests.
- **Responsable :** Amine
- **Statut :** Ouvert

## R2 — Retard des fonctionnalités Unity

- **Risque :** Parce que le TP UML doit être remis le 24 novembre et le jeu Unity le 29 novembre, il est possible que BF-02, BF-03 ou BF-04 prennent du retard, ce qui pourrait compromettre la remise du jeu.
- **BF touchés :** BF-02, BF-03, BF-04
- **Catégorie :** Planification
- **P :** 2 (les deux remises sont rapprochées) · **I :** 3 (la remise du projet peut être compromise) · **Criticité :** 6 (élevée)
- **Stratégie :** Réduire
- **Mitigation :** Inscrire une date de test avant le 22 novembre dans les issues BF-02, BF-03 et BF-04, puis vérifier leur avancement le 22 novembre.
- **Déclencheur :** Le 22 novembre, au moins une des fonctionnalités BF-02, BF-03 ou BF-04 n'est pas testable.
- **Contingence :** Utiliser une animation, un effet de particules et un son simples, puis consacrer le temps restant aux tests avant le 29 novembre.
- **Responsable :** Amine
- **Statut :** Ouvert

## R3 — Compteur mal affiché

- **Risque :** Parce que BF-05 doit afficher le compteur de pommes à la résolution 1280 × 720 (BNF-02), il est possible que le compteur sorte de l'écran, ce qui rendrait une information essentielle illisible.
- **BF touchés :** BF-05
- **Catégorie :** Exigences
- **P :** 1 (aucun souci d'affichage n'est signalé dans les issues actuelles) · **I :** 3 (BF-05 est Essentiel) · **Criticité :** 3 (moyenne)
- **Stratégie :** Réduire
- **Mitigation :** Tester la scène à 1280 × 720 et ajouter à l'issue BF-05 une capture montrant le compteur entièrement visible.
- **Déclencheur :** —
- **Contingence :** —
- **Responsable :** Amine
- **Statut :** Ouvert

## R4 — Retard causé par une absence

- **Risque :** Parce que les BF-01 à BF-08 sont tous confiés à une seule personne, il est possible qu'une absence d'une journée reporte les tests, ce qui entraînerait un ou deux jours de retard.
- **BF touchés :** Tout le projet
- **Catégorie :** Humain
- **P :** 2 (la répartition actuelle repose sur une personne) · **I :** 2 (un ou deux jours perdus, sans BF retiré) · **Criticité :** 4 (moyenne)
- **Stratégie :** Réduire
- **Mitigation :** À la fin de chaque séance de travail, enregistrer les changements du jeu sur GitHub et noter les tests restants dans l'issue du registre.
- **Déclencheur :** —
- **Contingence :** —
- **Responsable :** Amine
- **Statut :** Ouvert

## R5 — Fonctionnalités marquées terminées trop tôt

- **Risque :** Parce que les issues BF-01 à BF-08 décrivent les fonctionnalités sans expliquer comment les tester, il est possible qu'un BF soit marqué terminé trop tôt, ce qui entraînerait un ou deux jours de corrections.
- **BF touchés :** Tout le projet
- **Catégorie :** Communication
- **P :** 2 (les issues actuelles ne contiennent pas de test de validation) · **I :** 2 (un ou deux jours de corrections, sans BF retiré) · **Criticité :** 4 (moyenne)
- **Stratégie :** Réduire
- **Mitigation :** Ajouter un commentaire avec un test précis dans chaque issue BF-01 à BF-08 avant de la déplacer dans Done.
- **Déclencheur :** —
- **Contingence :** —
- **Responsable :** Amine
- **Statut :** Ouvert

## R6 — Son de ramassage trop fort

- **Risque :** Parce que BF-04 joue un son à chaque pomme attrapée, il est possible que le volume soit trop fort, ce qui demanderait moins d'une journée de réglage.
- **BF touchés :** BF-04
- **Catégorie :** Technique
- **P :** 1 (aucun problème de volume n'est signalé pour le moment) · **I :** 1 (moins d'une journée de réglage, aucun BF retiré) · **Criticité :** 1 (faible)
- **Stratégie :** Accepter
- **Mitigation :** —
- **Déclencheur :** —
- **Contingence :** —
- **Responsable :** Amine
- **Statut :** Ouvert
