import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error, mean_squared_error
from sklearn.preprocessing import StandardScaler
import joblib

# 1. Criar/ler a base de dados
# (Nesse caso, já terá esses dados coletados)
data = {
    'temperatura': [25, 22, 18, 20, 23, 19, 17, 21, 24, 20],
    'pressao': [1012, 1015, 1018, 1016, 1013, 1017, 1019, 1014, 1011, 1016],
    'umidade': [60, 75, 82, 78, 65, 80, 85, 70, 58, 77],
    'chuva': [0, 2.5, 5.1, 3.8, 0.5, 4.2, 6.0, 1.2, 0, 3.5]
}

df = pd.DataFrame(data)

# 2. Preparar os dados
X = df[['temperatura', 'pressao', 'umidade']]  # Features
y = df['chuva']  # Target

# Dividir em conjuntos de treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Normalizar os dados (opcional, mas recomendado para muitos modelos)
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)

# 3. Criar e treinar o modelo
model = RandomForestRegressor(n_estimators=100, random_state=42)
model.fit(X_train_scaled, y_train)

# 4. Avaliar o modelo
y_pred = model.predict(X_test_scaled)

print(f'MAE: {mean_absolute_error(y_test, y_pred):.2f} mm')
print(f'MSE: {mean_squared_error(y_test, y_pred):.2f} mm²')
print(f'RMSE: {np.sqrt(mean_squared_error(y_test, y_pred)):.2f} mm')

# 5. Salvar o modelo para usar no app
joblib.dump(model, 'modelo_previsao_chuva.pkl')
joblib.dump(scaler, 'scaler.pkl')

# 6. Exemplo de como fazer uma previsão
def prever_chuva(temperatura, pressao, umidade):
    # Carregar modelo e scaler
    model = joblib.load('modelo_previsao_chuva.pkl')
    scaler = joblib.load('scaler.pkl')
    
    # Preparar entrada
    entrada = np.array([[temperatura, pressao, umidade]])
    entrada_scaled = scaler.transform(entrada)
    
    # Fazer previsão
    return model.predict(entrada_scaled)[0]

# Testar a função
print(f"Previsão para 20°C, 1015hPa, 75% umidade: {prever_chuva(20, 1015, 75):.2f} mm")
