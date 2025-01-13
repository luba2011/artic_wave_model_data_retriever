## Setting Up the Project
The folder `notebooks` has to jupyter notebooks:
1. `Retrieve-data-Marine-Copernicus.ipynb`: To download and process the required data.
2. `File_creation.ipynb`: To process and create one file per chosen variable.
### Prerequisites:
- Python 3.x
- Virtual environment
- Copernicus credentials

### Installation:
1. Open cmd.
2. Navigate to the directory where you want the store the repository. --> cd path/to/your/directory.
3. Clone the repository: git clone https://github.com/luba2011/artic_wave_model_data_retriever.git
4. Create a virtual environment in the root directory, activate it and install the packages in `requirements.txt`
   - python -m venv your_venv_name
   - pip install -r requirements.txt
   - Add the venv to the Jupyter Notebooks (pip install ipykernel, python -m ipykernel install --user --name=your-venv-name --display-name "Your Virtual Environment")
5. Create a `.env` file and add your Copernicus username and password:

COPERNICUS_USERNAME="your_username"

COPERNICUS_PASSWORD="your_password"
6. Create a folder structure for storing the data as follows:
- Create a folder named `data` in the project root directory.
- Inside the `data` folder, create the following subfolders:
   - `raw_data`: This folder will contain the original, unprocessed datasets. Download a file of any day from https://data.marine.copernicus.eu/product/ARCTIC_MULTIYEAR_WAV_002_013/files?subdataset=cmems_mod_arc_wav_my_3km_PT1H-i_202012 and add in this folder.
   - `filtered_data`: This folder will store the processed and cleaned datasets.
7. In the notebooks change the root of the project:
os.chdir(r"path/to/your/directory")
8. Run the notebooks and the required files will be saved in the folder `filtered_data`


