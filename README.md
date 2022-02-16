Wine_Quality_Predication
Objective : To predict the quality of the wine by using some features like fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol quality

ProfileReport
ProfileReport is a Python library for dealing with analyzing and visualizing the data .

Installation
Use the package manager from pandas_profiling .

from pandas_profiling import ProfileReport
Usage
df=pd.read_csv("read the data")
df.head()
Build Model
from sklearn.ensemble import BaggingClassifier
from sklearn.neighbors import KNeighborsClassifier
knn=KNeighborsClassifier()

train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=30)
Fitting the model
knn.fit(x_train,y_train)
Hyperparameter
param_grid={'algorithm':['ball_tree','kd_tree','brute'],
            'leaf_size':[10,12,35,68,23,45,15],
            'n_neighbors':[3,5,8,9,10,12,13,15,20,30]
            
    
}
Accuracy Score
knn.score(x_train,y_train)
knn.score(x_test,y_test)
Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

License
MIT

