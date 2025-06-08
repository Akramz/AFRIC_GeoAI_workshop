[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Akramz/AFRIC_GeoAI_workshop/blob/main/GeoAI_workshop.ipynb)

# AFRIC GeoAI Workshop - Local Setup

This repository contains the materials for the AFRIC 2: Introduction to GeoAI workshop. The workshop covers geospatial data analysis using machine learning techniques including tabular ML with LightGBM and deep learning approaches.

## Environment Setup

### Prerequisites
- [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
- Python 3.8 or higher

### Creating the Conda Environment

1. **Clone this repository:**
   ```bash
   git clone https://github.com/Akramz/AFRIC_GeoAI_workshop
   cd AFRIC_GeoAI_workshop
   ```

2. **Create a new conda environment:**
   ```bash
   mamba create -n geoai python=3.12.3
   ```

3. **Activate the environment:**
   ```bash
   conda activate geoai
   ```

4. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Install additional conda packages for geospatial support:**
   ```bash
   mamba install -c conda-forge gdal geos proj
   ```

6. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook GeoAI_workshop.ipynb
   ```

## Workshop Content

The notebook covers:
- **Introduction to Geospatial Data**: Vector and raster data primitives
- **Problem Framing**: Crop type classification in Africa
- **Approach 1**: Tabular Learning with LightGBM
- **Approach 2**: Deep Learning with Sequence-to-One models

## GPU Support (Optional)

For deep learning sections, GPU acceleration is recommended:

```bash
# For CUDA-enabled GPUs
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

## Troubleshooting

If you encounter issues with geospatial libraries:

1. **GDAL installation issues:**
   ```bash
   conda install -c conda-forge gdal
   ```

2. **Shapely/GEOS issues:**
   ```bash
   conda install -c conda-forge geos
   ```

3. **Memory issues with large datasets:**
   - Ensure you have at least 8GB RAM available
   - Close other applications when running the notebook

## Data Files

The notebook automatically downloads required data files. Ensure you have internet connectivity when first running the data download cells.

## Authors

- Akram Zaytar
- Gilles Q. Hacheme  
- Aisha Alaagib
- Girmaw A. Tadesse 