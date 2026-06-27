# Dataset & Model Files

This folder contains files used in the asteroid light-curve modeling workflow: raw ephemeris/geometry data, processed telescope data, a merged normalized light-curve product, and the final convex-shape model.

---

## 1) `AstDySdata_all.txt`
**What it is:**  
All available asteroid-related data downloaded from the **AstDyS** website (Asteroids—Dynamic Site).

**What it typically contains:**  
AstDyS-provided observational/ephemeris and geometry information associated with the target asteroid (e.g., observing epochs and viewing/illumination geometry, depending on the AstDyS export you used).

---

## 2) `LBTdata.csv`
**What it is:**  
Data processed from **LBT** observations (after your reduction/cleaning pipeline).

**What it typically contains:**  
Observation time series and photometry products derived from LBT data (e.g., time, flux/magnitude, and optional metadata depending on your pipeline output).

---

## 3) `NormalizedLightCurve.txt`
**What it is:**  
A combined light-curve product with **normalized flux**, including distances in the asteroid-centered ecliptic coordinate system.

**Description (for the file header/comment):**  
**Light curves (flux) and distances from the asteroid-centered ecliptic coordinate system (AU).**

**Role in this project:**  
This is the main input light-curve dataset used for fitting/inversion, where flux values have been normalized (e.g., by a per-curve mean/median, depending on the script used).

---

## 4) `model_cv.obj`
**What it is:**  
The fitted **convex polyhedral asteroid shape model** in `.obj` format.

**Role in this project:**  
Represents the best-fit convex shape (mesh) obtained from the light-curve inversion/fitting procedure.  
You can open it in common 3D viewers (e.g., MeshLab, Blender) to visualize the asteroid model.

---

## Quick summary
- `AstDySdata_all.txt` — all asteroid data from AstDyS  
- `LBTdata.csv` — processed LBT dataset  
- `NormalizedLightCurve.txt` — merged, normalized light curve + asteroid-centered ecliptic distances (AU)  
- `model_cv.obj` — fitted convex polyhedral asteroid model
