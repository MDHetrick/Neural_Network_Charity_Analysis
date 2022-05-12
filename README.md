# Neural_Network_Charity_Analysis

### Optimizations
#### Attempt 1 
```
drop_list = ['IS_SUCCESSFUL', 'APPLICATION_TYPE_Other'] 

target = new_df['IS_SUCCESSFUL'].values
X = new_df.drop(drop_list,1).values


# Split the preprocessed data into a training and testing dataset
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X,target, random_state=1)


hidden_nodes_layer_1 = 80
hidden_nodes_layer_2 = 30

nn = tf.keras.models.Sequential()

# First hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_1, activation="relu", input_dim=input_features))

# Second hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_2, activation="relu"))

# Output layer
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))

```
Attempt 1: Loss = 0.5786486864089966, Accuracy = 0.7153352499008179


#### Attempt 2
```
drop_list = ['IS_SUCCESSFUL', 'APPLICATION_TYPE_Other',        'CLASSIFICATION_C1000', 'CLASSIFICATION_C1200', 'CLASSIFICATION_C2000', 
'CLASSIFICATION_C2100', 'CLASSIFICATION_C3000', 'CLASSIFICATION_Other',] 

target = new_df['IS_SUCCESSFUL'].values
X = new_df.drop(drop_list,1).values


# Split the preprocessed data into a training and testing dataset
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X,target, random_state=1)


hidden_nodes_layer_1 = 80
hidden_nodes_layer_2 = 30

nn = tf.keras.models.Sequential()

# First hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_1, activation="relu", input_dim=input_features))

# Second hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_2, activation="relu"))

# Output layer
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))
```
Attempt 2: Loss = 0.5963229537010193, Accuracy = 0.7021574378013611


#### Attempt 3
```
drop_list = ['IS_SUCCESSFUL', 'APPLICATION_TYPE_Other'] 

target = new_df['IS_SUCCESSFUL'].values
X = new_df.drop(drop_list,1).values


# Split the preprocessed data into a training and testing dataset
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X,target, random_state=1)


hidden_nodes_layer_1 = 80
hidden_nodes_layer_2 = 30

nn = tf.keras.models.Sequential()

# First hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_1, activation="relu", input_dim=input_features))

# Second hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_2, activation="tanh"))

# Output layer
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))

```
Attempt 3: Loss = 0.576120913028717, Accuracy = 0.7141690850257874

#### Attempt 4
```
drop_list = ['IS_SUCCESSFUL', 'APPLICATION_TYPE_Other'] 

target = new_df['IS_SUCCESSFUL'].values
X = new_df.drop(drop_list,1).values


# Split the preprocessed data into a training and testing dataset
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X,target, random_state=1)


hidden_nodes_layer_1 = 80
hidden_nodes_layer_2 = 5

nn = tf.keras.models.Sequential()

# First hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_1, activation="relu", input_dim=input_features))

# Second hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_2, activation="tanh"))

# Output layer
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))

```
Attempt 4: Loss = 0.5747625827789307, Accuracy = 0.7121865749359131

#### Attempt 5
```
drop_list = ['IS_SUCCESSFUL', 'APPLICATION_TYPE_Other'] 

target = new_df['IS_SUCCESSFUL'].values
X = new_df.drop(drop_list,1).values


# Split the preprocessed data into a training and testing dataset
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(X,target, random_state=1)


hidden_nodes_layer_1 = 105
hidden_nodes_layer_2 = 52
hidden_nodes_layer_3 = 5

nn = tf.keras.models.Sequential()

nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_1, activation="relu", input_dim=input_features))

# Second hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_2, activation="relu"))

# Third hidden layer
nn.add(tf.keras.layers.Dense(units=hidden_nodes_layer_3, activation="tanh"))

# Output layer
nn.add(tf.keras.layers.Dense(units=1, activation="sigmoid"))

```

Attempt 5: Loss = 0.5741150379180908, Accuracy = 0.7137026190757751