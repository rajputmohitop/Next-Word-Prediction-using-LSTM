# Environment setup (Conda)

Steps to create and use the conda environment for this project:

1. Create the environment from the provided file:

   ```bash
   conda env create -f environment.yml
   ```

2. Activate it:

   ```bash
   conda activate next-word-pred
   ```

3. (Optional) If you prefer using the project's `requirements.txt` instead of the embedded pip section, run:

   ```bash
   pip install -r requirements.txt
   ```

4. Verify TensorFlow is installed:

   ```bash
   python -c "import tensorflow as tf; print(tf.__version__)"
   ```

5. Run the app (example using Streamlit):

   ```bash
   streamlit run app.py
   ```

Notes:
- This environment.yml pins Python to 3.10 for compatibility with TensorFlow 2.15.0. If you have a GPU and want GPU-enabled TensorFlow, install the appropriate `tensorflow` package for your CUDA/cuDNN (see TensorFlow docs).
- If you encounter issues, try updating conda (`conda update -n base -c defaults conda`) and re-creating the env with `conda env create -f environment.yml --force`.
