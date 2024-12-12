import matplotlib.pyplot as plt
import matplotlib.patches as mpatches

# Création de la figure et de l'axe
fig, ax = plt.subplots(figsize=(8, 6))
ax.set_xlim(0, 10)
ax.set_ylim(0, 10)
ax.axis('off')

# Ajout des éléments du schéma
# Saponines
saponines = mpatches.Circle((3, 7), 1, edgecolor='green', facecolor='lightgreen', linewidth=2)
ax.add_patch(saponines)
ax.text(3, 7, 'Saponines', color='green', fontsize=10, ha='center', va='center')

# ROS (Reactive Oxygen Species)
ros = mpatches.Circle((7, 7), 1, edgecolor='red', facecolor='pink', linewidth=2)
ax.add_patch(ros)
ax.text(7, 7, 'ROS', color='red', fontsize=10, ha='center', va='center')

# Flèches pour montrer l'effet
ax.arrow(4.5, 7, 1.5, 0, head_width=0.3, head_length=0.3, fc='gray', ec='gray')
ax.text(5.5, 7.2, 'Neutralisation', fontsize=9, color='black', ha='center')

# Effet protecteur (aura verte)
aura = mpatches.Circle((3, 7), 1.5, edgecolor='green', facecolor='none', linestyle='dashed', linewidth=1.5)
ax.add_patch(aura)
ax.text(3, 5.5, 'Effet antioxydant', color='green', fontsize=9, ha='center')

# Titre
ax.text(5, 9.5, "Effet des saponines d'asperge sur les ROS", fontsize=12, color='black', ha='center', va='center')

# Afficher le schéma
plt.show()

