import numpy as np
import matplotlib.pyplot as plt

# Parámetros del tanque y el orificio
R = 1  # Radio del tanque en metros
d = 0.01  # Diámetro del orificio en metros

# Aceleración debido a la gravedad
g = 9.8  # m/s²

# Crear el arreglo de alturas
y = np.linspace(0, R, 1000)  # Intervalo de alturas desde 0 hasta el radio del tanque

# Calcular la velocidad de descenso dy/dt para cada altura
dy_dt = -(2 * g * y)**0.5

# Graficar dy/dt en función de y
plt.plot(y, dy_dt)
plt.xlabel('Altura (m)')
plt.ylabel('Rapidez de descenso (m/s)')
plt.title('Rapidez de descenso vs. Altura')
plt.grid(True)
plt.show()

# Encontrar el nivel del agua para un tiempo de 30 segundos
t = 30  # segundos
y_30s = R - (g * t**2 / 8)**0.5

print("El nivel del agua para t = 30 segundos es:", y_30s, "metros")
plt.plot(t, y_mm)
plt.xlabel('Tiempo (seg)')
plt.ylabel('Altura (mm)')
plt.title('Altura vs. Tiempo')
plt.grid(True)
plt.savefig('grafica.png')
