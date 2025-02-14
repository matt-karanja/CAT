import pandas as pd
data = pd.read_csv('path_to_your_data.csv')

print(data.head())
print(data.describe())
print(data.info())

data.dropna(inplace=True)  # Example: Remove missing values

data.fillna(method='ffill', inplace=True)

data = pd.get_dummies(data, columns=['categorical_column'])

from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
data_scaled = scaler.fit_transform(data)

processed_data = DataFrame(data_scaled, columns=data.columns)
processed_data.to_csv('processed_data.csv', index=False)
# CAT
