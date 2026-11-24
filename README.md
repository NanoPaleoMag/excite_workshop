# SIGMA/ Hyperspy Excite Workshop
Repository for excite workshop in December 2026

Please download all files ahead of the workshop.

Any issues with installation, please contact Thomas Ginnis at tg412@cam.ac.uk
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

### Hyperspy Installation 
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


  
### SIGMA2 Installation 


1. Open the conda Command Line Interface
   The terminal should look like (depending on your machine)
   ```
   (base) USERNAME@machine :
   ```

   If it says `(hyperspy)` instead of `(base)` - you are still in the hyperspy virtual environment. Run `conda deactivate` to return to `(base)`
3. Create a new conda environment for SIGMA2 by running the following
   ```
   conda create -n sigma2 python=3.10
   ```
   (you will need to press `y` to confirm the installation)
4. Activate the sigma2 environment by running:
   ```
   conda activate sigma2
   ```
   The terminal will now look like:
   ```
   (sigma2) USERNAME@machine :
   ```
   
6. Download the latest version of SIGMA2 from https://github.com/NanoPaleoMag/SIGMA2 by pressing the green `<> Code` button
7. Extract the downloaded zip file to a suitable location on your PC (eg. `Documents/SIGMA2`)
   
8. Using the conda terminal, navigate to this folder. You can do this by running the following (replacing the path with where you extract the files to)
   ```
   cd Documents/SIGMA2

   ```
   The terminal should now look something like
   ```
   (sigma2) C:\Users\USERNAME\Documents\SIGMA2
   ```

9. Install the requirements for SIGMA2 by running:
    ```
    pip install -r requirements.txt
    ```
    And following the instructions in the terminal
    
10. Once the `pip` installer has finished, open a jupyter notebook by running
    ```
    jupyter lab
    ```

11. In the browser that pops up, navigate to the `tutorials` folder and open `Interactive_SEM_tutorial`
12. Run the first cells by pressing `Shift`+`Enter`. The cells will show `[*]` while running, and will show `[1]` once they are finished.
13. If the cells run correctly, then SIGMA is installed correctly



