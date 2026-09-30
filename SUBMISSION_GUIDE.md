# Publishing and submitting the assignment

You have a completed notebook and project folder. The Kaggle and GitHub URLs for your work are created when you publish under your own accounts. They have not been created for you here.

Your teacher most likely expects your own Kaggle notebook link and your GitHub repository link. Include the original dataset link separately as a source. A dataset page alone does not show your completed assignment.

## 1. Download the files
Download `Adult_Income_Project.zip` and extract it on your computer (Windows: right-click the ZIP and select Extract All). Open the `adult-income-eda` folder inside it. You can also download the notebook separately.

## 2. Publish the Kaggle notebook
1. Sign in at https://www.kaggle.com/.
2. Open https://www.kaggle.com/datasets/wenruliu/adult-income-dataset and choose New Notebook. You can also start from Code > New Notebook and attach the dataset yourself.
3. In the notebook editor, use File > Import Notebook (the label may be Upload Notebook) and choose `Adult_Income_Cleaning_EDA.ipynb`.
4. Set the title to `Adult Income - Cleaning, EDA and Feature Engineering`.
5. Check the Input/Data panel. If the Adult Income dataset is absent, choose Add Input/Add Data, search `wenruliu/adult-income-dataset`, and add it. The loader finds `adult.csv` under `/kaggle/input/` automatically.
6. Select Run All. Check that the cells finish without errors and all six charts appear. GPU is not needed.
7. Choose Save Version and select Save & Run All (or the equivalent option that runs and saves outputs). Wait for the saved run to finish successfully.
8. Open Share or the notebook visibility settings and change visibility to Public if your teacher requires public access. Save the visibility change.
9. Open the saved notebook page and copy its URL. It usually has the shape `https://www.kaggle.com/code/YOUR_USERNAME/YOUR_NOTEBOOK_SLUG`.
10. Open that link in a private/incognito window to confirm your teacher can view it. Copy the actual URL from Kaggle; the example above is only a format.

Kaggle menu labels can vary slightly. Notebook reference: https://www.kaggle.com/docs/notebooks

## 3. Publish the GitHub repository
1. Sign in at https://github.com/ and open https://github.com/new.
2. Use `adult-income-eda` as the repository name. Add a short description such as: `Data cleaning, exploratory analysis and feature engineering on the Adult Income dataset`.
3. Select Public if your teacher needs public access. Select Add a README, then Create repository.
4. Open Add file > Upload files. Drag the CONTENTS of the extracted `adult-income-eda` folder into the upload area. Include the notebook, README.md, requirements.txt, SUBMISSION_GUIDE.md, data folder and outputs folder. The supplied README replaces the starter README. Upload the extracted files, not just the ZIP.
5. Enter a commit message such as `Add completed Adult Income EDA assignment`, then choose Commit changes or the displayed confirmation. If GitHub proposes a branch and pull request, complete that flow and merge it so the files appear on the default branch.
6. Open the uploaded notebook and check that code, tables and charts are visible. GitHub displays saved notebook outputs; it does not run the notebook.
7. Copy the repository URL from your browser. It usually has the shape `https://github.com/YOUR_USERNAME/adult-income-eda`.
8. Add your real Kaggle notebook URL to README.md using the pencil/edit button and save the edit. You can also add the GitHub link to the first Markdown cell of your Kaggle notebook and save a new version.
9. Test the repository link in an incognito window. If your teacher requires a private repository, follow their collaborator-access instructions instead.

GitHub documentation:
- https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository
- https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository

## 4. Submit
Submit the actual notebook file if requested, plus:

- Kaggle notebook link: paste your published notebook URL.
- GitHub repository link: paste your repository URL.
- Dataset source: https://www.kaggle.com/datasets/wenruliu/adult-income-dataset
- Five findings: included in the notebook and `outputs/five_key_insights.md`.

Do not submit placeholder URLs containing YOUR_USERNAME. Review the notebook and understand its cleaning choices before submission. The assignment asks for cleaning, EDA and feature engineering; no trained model is needed.

## Optional: run in Google Colab
Open https://colab.research.google.com/, choose Upload notebook and select the `.ipynb`. In the left Files sidebar, upload `data/adult.csv` from the extracted folder. Then choose Runtime > Run all. The loader also checks `/content/adult.csv`.
