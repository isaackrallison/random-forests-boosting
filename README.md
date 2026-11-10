# Random Forests & Boosting Lab

An interactive study guide for §18.4–18.5.4 of Kevin P. Murphy, *Probabilistic Machine Learning: An Introduction*
(random forests, additive models, forward stagewise fitting, least squares boosting, AdaBoost and LogitBoost).

**Live:** https://isaackrallison.github.io/random-forests-boosting/

Every section has an **Explain it** box at four levels (Kid, High school, Undergrad, Grad / MLE), switchable globally from the top bar.

- **18.4 Random forests:** Fig. 18.5 grown live. 200 bagged trees, 200 random-forest trees and 200 boosted trees on a spam-like data set, with test error vs number of trees. A root-split histogram, single-tree error and tree correlation ρ show why the forest wins (ρσ² + (1 − ρ)σ²/M). Sweep m from 1 to 30, and compute the real spam features (word and character frequencies, CAPAVE, CAPMAX, CAPTOT) from an email you edit.
- **18.5 Boosting:** the same trees bagged vs boosted on a 1-D curve. Bagged stumps stay a step (bias), boosted stumps trace the curve, and full trees reverse the picture.
- **18.5.1 Forward stagewise:** solve Eq. 18.17 by brute force with a sign stump. Plot the loss for every threshold and the line search in β under squared, absolute or Huber loss, with optional outliers.
- **18.5.2 Least squares boosting:** Fig. 18.6 step by step. Residuals and the new tree on the left, the running ensemble on the right, and train/test MSE vs m.
- **18.5.3 AdaBoost:** Fig. 18.7 loss curves vs margin, a numerical check that exponential and log loss share the minimizer ½ log(p/(1 − p)), and AdaBoost.M1 on a circle problem with weight-sized points, err_m, α_m, the exp-loss training bound, and the "new weights give err = ½" check.
- **18.5.4 LogitBoost:** influence |∂ℓ/∂f| vs margin (unbounded vs capped at 2), then AdaBoost vs LogitBoost (Algorithm 18.2) on flipped labels, with test error and test log loss of the Eq. 18.36 probabilities.
- A 42-question quiz tagged by level and a cheat sheet.

Single self-contained `index.html`, no build step. Loads Google Fonts and MathJax from cdnjs. All data are synthetic and generated in the page from fixed seeds. The spam-like set only borrows feature names from the HP spam data. Every tree, forest and boosted ensemble is fit live in the browser with an exact weighted CART split search.
