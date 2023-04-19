# arbilex_case_study

![plot](./images/bert_clusters.png)

# Files & Folders

To load the repo locally run:
```
git clone https://github.com/daniel-bejarano/arbilex-exercise.git
cd arbilex-exercise
```

Below are the relevant files and their description:
- `Arbilex Case Study.ipynb`
    - This file contains all the code used to perform the exercise. It also includes displays of relevant visuals and the "Writeup" section at the end contains my analysis and discussion of results. It contains 4 main sections. 
        1. STEUP is just imports
        2. PART I of the exercise, including scraping and text content extraction
        3. PART II, which includes cleaning the text data, N-gram analysis, TF-IDF clustering, and BERT clustering (didn't have time for LDA).
        4. WRITEUP as described above.<br>
    - To view the file in the state that I uploaded, including images from which I based my analysis, go here:
    https://nbviewer.org/github/daniel-bejarano/arbilex-exercise/blob/main/Arbilex%20Case%20Study.ipynb
- `output_files/`
    - This folder contains every one of the scraped opinion PDFs, saved as JSONs: `opinion_<case_number>.json`. The folder also includes a file called `all_opinions.json` that has all the contents from those 1000 individual files. There is also a csv files, `all_opinions.csv`, containing the data stored as I performed the exercise, for easy saving and loading.
- `output_files_test/`
    - This folder contains the same documents as `output_files/` but for a subset of the data. I set up the `Arbilex Case Study.ipynb` file so you can run it and all data will be saved here, but it will load data from `output_files/`. That way you can run the notebook from beginning to end without having to wait too long for it to finish, while also preserving the original data.
- `images/`
    - You can ignore this one. It's just images for this README file.
- `PDFs/`
    - Also can be ignored. This folder holds temporary PDF files as they are downloaded to be OCRed.

![plot](./images/notebook.png)

# Running the Exercise
To run this exercise you simply need to run the `Arbilex Case Study.ipynb` file from an IPython service. The notebook is set up to compute using partial data at every step to speed things up, but when it loads data it loads the actual full set of data, which I pre-ran. It requires several dependencies, which are all found in the `requirements.txt` file. It's a messy requirements file as I didn't have time to clean it, but it should be complete. You most likely know this well, but one way to set up the environment is:
```
conda create -n dan_exercise_env python=3.8
conda activate
pip install -r requirements.txt
python -m ipykernel install --user --name="Dan_Exercise_Env"
```

Now make sure to activate your IPython kernel using that environment. From there you can run the notebook.

NOTE: There's two files that are a little big (~20MB), and although they are smaller than Github's soft limit of 50MB, sometimes with slow internet connection there's issues. If you have problems with them, try adding Git LFS:
```
brew install git-lfs
git lfs install
```

If you have any questions, please don't hesitate to contact me :)
