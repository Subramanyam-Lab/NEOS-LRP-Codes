#  Codes and datasets for the paper Neural Embedded Optimization for Integrated Location and Routing Problems
-------------------------------------------------
### Random Route Costs and Number of Routes in branch random_learning_prediction

In the random_learning_prediction branch of this repository, we have introduced a  change to the way route costs and the number of routes are determined in the NEOS LRP model. Instead of using the `rho` neural network to predict these values, we are now generating them randomly within predefined ranges.

#### Key Changes in This Branch:
- **Route Cost Calculation**: Route costs for each depot are now randomly generated within the range of 0.0 to 25.3265 (this range is obtained from training data and is the normalized cost).
- **Number of Routes Estimation**: The number of routes for each depot is randomly chosen between 1 and 19, instead of being predicted by the `rho` neural network.(this range is obtained from training data).
  
#### Adaptations in the Code:
- In the `lrp_easy` script, the section where the `rho` neural network was previously used has been modified to incorporate the random value generation.
- The random values are used as constraints in the Gurobi optimization model. 

#### Running the Code in This Branch:
- The steps to run the code in this branch are similar to those in the main branch, with the key difference being the way route costs and the number of routes are handled.
- Users should be aware of these changes and consider their implications when interpreting the results.
The repository is structured as follows: 
-------------------------------------------------
