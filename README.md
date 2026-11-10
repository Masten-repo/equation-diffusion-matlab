# Équation de diffusion avec terme dissipatif : analyse spectrale et schémas aux différences finies

Résolution de l'EDP **u_t = u_xx − αu** avec conditions de Dirichlet homogènes, en MATLAB. Travail pratique de *Technique de modélisation* (M1 CHPS, UVSQ – Université Paris-Saclay), réalisé en binôme.

## Contenu du travail

- **Solution analytique** par séparation des variables et projection sur la base de Fourier, pour deux conditions initiales : sin(2πx) et un signal triangulaire.
- **Trois schémas aux différences finies** : Euler explicite, Euler implicite et Crank-Nicolson.
- **Analyse de stabilité de Von Neumann** : condition de stabilité de l'explicite modifiée par le terme dissipatif (Δt ≤ 2Δx² / (4 + αΔx²)), stabilité inconditionnelle de l'implicite et de Crank-Nicolson.
- **Vérification empirique** : stabilité à 0,95 Δt_max, divergence à 1,02 Δt_max.
- **Implémentation vectorisée** avec matrices creuses (`sparse`) tridiagonales, système résolu par l'opérateur de division à gauche de MATLAB (complexité linéaire).
- **Analyse de la singularité** du signal triangulaire : lissage par l'implicite, légère oscillation parasite à l'apex avec Crank-Nicolson.

## Fichiers

- `rapport.pdf` : rapport complet (calculs, analyse de stabilité, résultats, annexes avec les codes MATLAB)

## Technologies

MATLAB
