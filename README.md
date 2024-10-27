import matplotlib.pyplot as plt
import seaborn as sns

top_10_altos = df.nlargest(10, 'Cost of Living')

plt.figure(figsize=(10, 6))
sns.barplot(x='Cost of Living', y='Countries', data=top_10_altos)
plt.title('Top 10 países con el costo de vida más alto')
plt.xlabel('Costo de Vida')
plt.ylabel('Países')
plt.show()


top_10_bajos = df.nsmallest(10, 'Cost of Living')

plt.figure(figsize=(10, 6))
sns.barplot(x='Cost of Living', y='Countries', data=top_10_bajos)
plt.title('Top 10 países con el costo de vida más bajo')
plt.xlabel('Costo de Vida')
plt.ylabel('Países')
plt.show()


paises_america = df[df['Countries'].isin(['list_of_american_countries'])]  # Reemplaza con la lista de países de América

plt.figure(figsize=(10, 6))
sns.barplot(x='Cost of Living', y='Countries', data=paises_america)
plt.title('Costo de vida de los países de América')
plt.xlabel('Costo de Vida')
plt.ylabel('Países')
plt.show()
