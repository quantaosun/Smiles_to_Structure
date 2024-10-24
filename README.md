# Smiles_to_Structure

This script reads a list of SMILES (Simplified Molecular Input Line Entry System) strings from a raw SMILES file, converts them into chemical structures using RDKit, and displays the resulting structures as images directly within a Jupyter notebook. Each structure is labeled with its corresponding entry number for easy identification.


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/quantaosun/Smiles_to_Structure/blob/main/smiles_to_image.ipynb)

Tutorial:
1. Generate a csv file, for example, for a specific protein target, you can download a csv file from Chembl database

 <img width="1361" alt="image" src="https://github.com/quantaosun/Smiles_to_Structure/assets/75652473/3cf5a98c-b25b-46a1-b4b1-16836ccd92c2">

 
2. Open this csv file with your excel or Mac number software, export it to csv again, since the downloaded csv may have some minor format issue not recognised by this code.

3. Upload this new csv file to the code via the Colab budge link, and it is ready to process through the SMILES inside the csv you provided.

4. read the file by modifying the file name ```df = pd.read_csv('11.csv')
df```

5. Change the column number based on where is your SMILES in the csv file, if they are stored at 9th column, it should be ```!awk -F "\"*,\"*" '{print $8}' 11.csv > smile.smi```

(6. Delete rows that not a SMILES, and export the new smiles string to a new csv file.)

Display the molecules as images inside Jupyter Notebook

<img width="1361" alt="image" src="https://github.com/quantaosun/Smiles_to_Structure/assets/75652473/0418e0f8-2291-429a-ab0b-f97c7f3cc056">
