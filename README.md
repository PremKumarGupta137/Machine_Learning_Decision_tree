# Decision Tree Using Entropy  
This implementation uses **Entropy** and **Information Gain** to build the decision tree. Entropy is a measure of impurity or uncertainty in the dataset. At each node, the algorithm calculates the entropy for all possible splits and selects the split with the highest **Information Gain**, aiming to reduce uncertainty and create purer subsets.  

## Key Details:  
- **Entropy Formula**:  
  \[
  \text{Entropy}(S) = - \sum_{i=1}^{c} p_i \log_2(p_i)
  \]  
  \( p_i \) represents the proportion of samples in class \( i \).  

- **Information Gain Formula**:  
  \[
  IG = \text{Entropy(Parent)} - \sum_{k} \left( \frac{|S_k|}{|S|} \times \text{Entropy}(S_k) \right)
  \]  
  \( S_k \) is the subset after the split.  

This method ensures that the tree selects features contributing most to reducing impurity at each step.

---

# Decision Tree Using Gini Index  
This implementation uses the **Gini Index** to build the decision tree. Gini Index measures impurity based on the probability of misclassification. The algorithm evaluates splits and selects the one with the lowest **Gini Impurity**, focusing on creating purer subsets efficiently.  

## Key Details:  
- **Gini Index Formula**:  
  \[
  \text{Gini}(S) = 1 - \sum_{i=1}^{c} p_i^2
  \]  
  \( p_i \) represents the proportion of samples in class \( i \).  

The Gini Index is computationally simpler than entropy, as it avoids logarithmic calculations. This makes it faster for larger datasets while ensuring effective tree construction.
