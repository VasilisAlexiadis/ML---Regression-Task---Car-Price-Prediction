# ML---Regression-Task---Car-Price-Prediction

Methodology:

1. We set the hyperparemeters of our models, employing mainly try and error method (however for Ridge, Lasso, Decision Trees and Random Forest after running Gridsearch we obtain an initial direction)

2. We trained our models using 5 variations of our dataset.

3. Best results are obtained utilizing data after Standardization, where 4 out of 6 models deliver better results because Standardization can improve models' performance in several ways:
    
    a. Improved optimization: Standardizing the data can make the optimization process more efficient. In particular, Neural networks are sensitive to the scale of the input data, and large differences in scale between features can cause the optimizer to take larger steps in some dimensions than others. This can slow down convergence and make the optimization process more unstable. By standardizing the data, all features are on the same scale, which can make the optimization process more stable and faster.
    
    b.Better feature learning: Standardizing the data can also help the model to learn better representations of the data. Large differences in scale between features can make it harder for the model to learn useful representations. By standardizing the data, all features are on the same scale, which can make it easier for the model to learn useful representations.

It's important to note that standardization should only be applied to the training data, and then the same transformation should be applied to the test and validation sets.

4. Decreased performance lower R2 score, for all models, after performing PCA. This can be explained as follows:
    
    a.Loss of important information: By reducing the dimensionality of the data, PCA can also discard some important information that the model needs to make accurate predictions. This is especially true if the number of principal components is set to be less than the number of original features.

    b.Overfitting: PCA is a linear technique and it can be sensitive to the presence of non-linear relationships in the data. If the data has a lot of non-linear relationships, PCA may not be the best technique to use. This can lead to overfitting if the model is too complex, and the PCA projection of the data is not representative of the original data.

    c.Noise: PCA is sensitive to noise in the data. If the data has a lot of noise, PCA may not be the best technique to use as it can amplify the noise and lead to worse performance.

    d.Data distribution: PCA is sensitive to the distribution of the data. If the data is not normally distributed, PCA may not be the best technique to use as it can lead to poor performance.

5. Decison Tree on PCA data performs pretty poorly. The reason is that Decision trees are prone to overfitting. They are unstable, meaning that a small change in the data can lead to a large change in the structure of the optimal decision tree


In general, it's recommended to try different preprocessing techniques and see which one performs the best on your specific problem. Also, it's important to keep in mind that preprocessing is not always necessary and it's not always the best step, it depends on the specific problem you are trying to solve.

Conclusions:

Best Model:

Random Forest performs best on all data preprocessing methods.

Reasons:
It is a type of ensemble model. Ensemble models combine the predictions of multiple simpler models to create a more accurate overall prediction. In the case of a Random Forest, this is done by training many decision trees on different subsets of the data, and then averaging the predictions of all of the decision trees. This helps to reduce overfitting and improve the overall accuracy of the model. Additionally, Random Forest model is robust to outliers and handle high dimensional data. Also, it is good at capturing non-linear interactions and decision boundaries.