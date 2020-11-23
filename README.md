# DSO670 Final Project

This project is for DSO 670 Seminar with Dr. Vishal Gupta at USC Marshall. 
This is a project of new experiments based on the Optimal Prescriptive Trees paper by Bertsimas et al. (2019).

# Summary 
This project is to prescription factor(mu) from Bertsimas et al. (2019), and see how outcome error of the trees vary with the variation of mu. First, I calculate the true oracle outcomes, estimate counterfactual outcomes with a KNN approach, and keep a baseline of the original prescribed outcomes. Then, I fit an OPT with varying mu values and compare the predicted outcomes prescribed by the tree to the calculated outcomes to provide outcome error. Further, I test each optimal mu that minimizes the outcome error in each method by using this mu to fit a tree and record treatment and outcome accuracies. The goal is to gain more insight in how the this prescription factor affects the optimal prescriptive tree performance.

# Sanity Check Experiment File
The sanity check experiment file tests the Personalized Job Training experiment from section 5.3 in "Optimal Prescriptive Trees." This runs an optimal prescriptive tree on the data from the LaLonde (1986) dataset, which can be found at http://users.nber.org/~rdehejia/nswdata2.html.

# Final Project File
The final project file predicts various outcomes and trains the OPTs with varying prescription factors to find the optimal mu that minimizes the outcome error. This includes an oracle function to find the true best outcomes, a baseline function that stores originally observed outcomes, and a KNN-CF function that computes the counterfactuals based on a KNN method. Lastly, we compute two base mu values that are cross validated on the data to gain an optimal prediction accuracy and prescription outcome. The optimal mus for each of these 5 methods are stored and can be used to test the optimal prescriptive trees to compare the treatment accuracy and outcome accuracy of the OPT(mu) for each value.


# References
This is a project based on "Optimal prescriptive trees" by Bertsimas, Dimitris and Dunn, Jack and Mundru, Nishanth (2019). 
I referenced the code from Interpretable AI, LLC, 2020, which can be found at https://www.interpretable.ai
