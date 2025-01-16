import matplotlib.pyplot as plt
import numpy as np

# Parameters for the spiral pattern
num_rings = 50  # Number of concentric rings
num_segments = 36  # Segments per ring
colors = ['purple', 'gold', 'white', 'pink']  # Colors for the checkerboard pattern

# Generate the figure again, this time ensuring the pattern covers all four quadrants
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_aspect('equal')
ax.axis('off')

# Generate the spiral checkerboard pattern for all quadrants
for r in range(num_rings):
    for s in range(num_segments):
        # Calculate angle and radius
        angle_start = (s / num_segments) * 2 * np.pi
        angle_end = ((s + 1) / num_segments) * 2 * np.pi
        radius_inner = r / num_rings
        radius_outer = (r + 1) / num_rings

        # Alternate colors
        color = colors[(r + s) % len(colors)]

        # Create a wedge (segment of a ring)
        wedge = plt.Polygon([
            (radius_inner * np.cos(angle_start), radius_inner * np.sin(angle_start)),
            (radius_outer * np.cos(angle_start), radius_outer * np.sin(angle_start)),
            (radius_outer * np.cos(angle_end), radius_outer * np.sin(angle_end)),
            (radius_inner * np.cos(angle_end), radius_inner * np.sin(angle_end))
        ], closed=True, facecolor=color, edgecolor='none')
        
        ax.add_patch(wedge)

# Display the full spiral pattern in all four quadrants
plt.xlim(-1, 1)
plt.ylim(-1, 1)
plt.show()



