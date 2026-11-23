# Excite Workshop
Repository for excite workshop in December 2026

Please download all files ahead of the workshop.

## Installation Instructions

### Conda
SIGMA and Hyperspy will use conda to manage and install packages. Follow these instructions to install the miniconda software.

1. Download the appropriate installer for windows / macOS here: https://www.anaconda.com/download/success?reg=skipped-miniconda&path=miniconda
2. Run the installer - the default options will generate a suitable environment to run SIGMA and Hyperspy
3. Once the installer has finished, open the conda Command Line Interface (CLI)
   * On windows, this is the Anaconda Prompt application, which should be in the start menu
   * On macOS / Linux, this is the standard Terminal application
   
   The terminal should look like (depending on your machine)
   ```
   (base) USERNAME@machine :
   ```
   
4. Run the following command to verify that `conda` is installed correctly :
   ```
   conda --version
   ```
   
   It should return something like:
   ```
   conda 25.3.1
   ```

### Hyperspy
1. Open the conda Command Line Interface
   The terminal should look like (depending on your machine)
   ```
   (base) USERNAME@machine :
   ```
3. Create a new conda environment for Hyperspy by running the following
   ```
   conda create -n hypesrspy_env -c conda-forge
   ```
   (you will need to press `y` to confirm the installation)
4. Activate the hyperspy environment by running:
   ```
   conda activate hyperspy_env
   ```
   The terminal will now look like:
   ```
   (hyperspy_env) USERNAME@machine :
   ```
   
6. Install Hyperspy by running the following. Note - we will install exspy -an extended version of hyperspy, which can deal with more electron microscopy datasets. It will automatically install the base hyperspy in addition
   ```
   conda install exspy -c conda-forge
   ```
   
7. Follow the instructions in the installer - you will need to press `y` to confirm the installation

8. Once the installer has finished, install `jupyterlab` with the following command
   ```
   conda install jupyterlab -c conda-forge
   ```

9. Open a jupyter lab terminal by running:
    ```
    jupyter lab
    ```

10. Create a new notebook, and run:
    ```
    import hyperspy
    hyperspy.__version__
    ```
    If hyperspy and jupyter are correctly installed, it should return the version number of the installed hyperspy `'2.3.0'`     
  



