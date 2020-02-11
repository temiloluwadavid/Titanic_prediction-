# Titanic_prediction-
This repository was to test my knowledge on classification algorithms 
you can use the grid search fo get the best parameters and model. 
I didnt use it here because my computer doesnt have a great processing power. 
find the code needed for the grid search below:
from sklearn.model_selection import GridSearchCV
parameters = [{'C': [1, 10, 100, 1000], 'kernel': ['linear']},
              {'C': [1, 10, 100, 1000], 'kernel': ['rbf'], 'gamma': [0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9]}]
grid_search = GridSearchCV(estimator = classifier,
                           param_grid = parameters,
                           scoring = 'accuracy',
                           cv = 10,
                           n_jobs = -1)
grid_search = grid_search.fit(x, y)
best_accuracy = grid_search.best_score_
best_parameters = grid_search.best_params_
