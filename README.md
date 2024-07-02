import matplotlib.pyplot as plt
import matplotlib.patches as mpatches

# Create the figure and axis
fig, ax = plt.subplots(figsize=(8, 6))

# Add the campaign rectangle
campaign_rect = mpatches.FancyBboxPatch((0.45, 0.8), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orange")
ax.add_patch(campaign_rect)
ax.text(0.5, 0.825, "Campaign", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

# Add the ad sets rectangles
ad_set1_rect = mpatches.FancyBboxPatch((0.25, 0.6), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="lightcoral")
ax.add_patch(ad_set1_rect)
ax.text(0.3, 0.625, "Ad Set 1", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

ad_set2_rect = mpatches.FancyBboxPatch((0.65, 0.6), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="lightcoral")
ax.add_patch(ad_set2_rect)
ax.text(0.7, 0.625, "Ad Set 2", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

# Add the ads rectangles under Ad Set 1
ad1_rect = mpatches.FancyBboxPatch((0.15, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad1_rect)
ax.text(0.2, 0.425, "Ad 1", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

ad2_rect = mpatches.FancyBboxPatch((0.25, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad2_rect)
ax.text(0.3, 0.425, "Ad 2", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

ad3_rect = mpatches.FancyBboxPatch((0.35, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad3_rect)
ax.text(0.4, 0.425, "Ad 3", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

# Add the ads rectangles under Ad Set 2
ad4_rect = mpatches.FancyBboxPatch((0.55, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad4_rect)
ax.text(0.6, 0.425, "Ad 4", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

ad5_rect = mpatches.FancyBboxPatch((0.65, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad5_rect)
ax.text(0.7, 0.425, "Ad 5", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

ad6_rect = mpatches.FancyBboxPatch((0.75, 0.4), 0.1, 0.05, boxstyle="round,pad=0.02", edgecolor="black", facecolor="orangered")
ax.add_patch(ad6_rect)
ax.text(0.8, 0.425, "Ad 6", horizontalalignment='center', verticalalignment='center', fontsize=12, color='white')

# Draw lines
ax.plot([0.5, 0.3], [0.8, 0.625], "k-")
ax.plot([0.5, 0.7], [0.8, 0.625], "k-")

ax.plot([0.3, 0.2], [0.6, 0.425], "k-")
ax.plot([0.3, 0.3], [0.6, 0.425], "k-")
ax.plot([0.3, 0.4], [0.6, 0.425], "k-")

ax.plot([0.7, 0.6], [0.6, 0.425], "k-")
ax.plot([0.7, 0.7], [0.6, 0.425], "k-")
ax.plot([0.7, 0.8], [0.6, 0.425], "k-")

# Set limits and hide axes
ax.set_xlim(0, 1)
ax.set_ylim(0, 1)
ax.axis('off')

# Save the plot to a file
plt.savefig("/mnt/data/linkedin_ad_structure.png")

# Show the plot
plt.show()
