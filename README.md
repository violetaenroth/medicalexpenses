# Insurance expenses

We have the following features to predict the charges of a policyholder in an insurance company:
<ul>
    <li> age: Age of the beneficiary.
    <li> sex: Beneficiary's sex (female/male).
    <li> bmi: Body mass index.
    <li> children: Number of children covered by the insurance.
 <li> smoker: Smoking (yes/no).
<li> region: The beneficiary's residential area in the US (northwest/northeast/southwest/southeast).
<li>charges: Individual medical costs billed by the insurance.
    </ul>
We used 1/3 of the observations as a test set and the rest to train the models. We compared multiple out-of-the box ML models by using cross-validation on the MSE and MEA mean and standard deviation as the measures of goodness of fit. The best ones were the random forest and the XGBoost regressor.  We then fined-tune these two models using a random GridSearchCV to find their optimal parameters, and a Pipeline to control the workflow. Finally, we compared the results with a neural network. We got almost as small errors with the neural network as the ones with the other models. Nevertheless, neural networks have a bigger variance in the MAE CV errors and also the computational time was much bigger. The conclusions are
<ul>
    <li> An important factor is the smoking feature: the charges are much bigger on people that smokes that on people that don't. The coefficients found on lineal regression and Random Forest algorithms tell us that these two features are very important.
        <li>Random Forest gives a good and fast fit: the Random Forest algorithm give us the smallest errors in comparison to other models. Moreover, the time to train this model was also small. This model has a good equilibrium between accuracy and computational time for the data that we were analyzing.
    </ul>
