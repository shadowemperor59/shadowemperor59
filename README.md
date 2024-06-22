import matplotlib.pyplot as plt
import numpy as np

# Create a figure and axis
fig, ax = plt.subplots()

# Draw the circle for the logo
circle = plt.Circle((0.5, 0.5), 0.4, color='black', fill=True)
ax.add_artist(circle)

# Define the dragon shape using a path
dragon_path = [
    (0.5, 0.75), (0.6, 0.65), (0.7, 0.75), (0.8, 0.7), (0.75, 0.6), 
    (0.85, 0.5), (0.75, 0.4), (0.8, 0.3), (0.7, 0.25), (0.6, 0.35), 
    (0.5, 0.25), (0.4, 0.35), (0.3, 0.25), (0.2, 0.3), (0.25, 0.4), 
    (0.15, 0.5), (0.25, 0.6), (0.2, 0.7), (0.3, 0.75), (0.4, 0.65), (0.5, 0.75)
]

# Split the path into x and y coordinates
dragon_x, dragon_y = zip(*dragon_path)

# Draw the dragon
ax.plot(dragon_x, dragon_y, color='white', lw=3)

# Set the aspect of the plot to be equal
ax.set_aspect('equal')

# Remove the axes
ax.axis('off')

# Show the logo
plt.show()
