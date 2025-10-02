
# Automated Birefringence-Based High-Resolution Orientation Mapping of Cellulose Nanofibrils

**Yasaman Asiaee<sup>1,2</sup>, Parinaz Rahimzadeh-Bajgiran<sup>1</sup>, Mehdi Tajvidi<sup>1,2</sup>\***  

<sup>1</sup> School of Forest Resources, University of Maine, 5755 Nutting Hall, Orono, ME 04469, USA  
<sup>2</sup> Advanced Structures and Composites Center, University of Maine, Orono, ME 04469, USA  

\* **Corresponding Author:** [mehdi.tajvidi@maine.edu](mailto:mehdi.tajvidi@maine.edu)








# iBOI method 
These  two methods use  for orienation mapping of cellulose  nanofibrils  film usin polarized light microscopy  image.
This script computes the Birefringence Orientation Index (BOI) from perpendicular-angle polarized images, finds the dominant fiber orientation per pixel, and outputs:

  1. a quiver (vector) plot of local fiber directions

  2. a colored bar chart of pixel counts per orientation bin

# Requirements

opencv-python, numpy, scipy, matplotlib

# Input

PNG images named by angle, e.g. -90_aligned.png, 0_aligned.png, … for each angle pair listed in angles_regular.

# How it works

  1. Loads all image pairs, extracts a centered 800×800 ROI.

  2. Computes pixel-wise BOI for each pair (using blue channel, with a threshold to skip noise).

  3. Selects the angle with maximum |BOI| at each pixel.

  4. Assigns orientation vectors & colors; downsamples for clarity.
