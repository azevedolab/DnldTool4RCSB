# DnldTool4RCSB: Download Tool for RCSB Structure
This Jupyter Notebook (dnldtool4rcsb.ipy) downloads files (PDB and SDF) with atomic coordinates from the Protein Data Bank. It reads the HTML RCSB page to scrape data related to the identification of the active ligand. It focuses on structures for which binding affinity data is available. The active ligand is a small molecule bound to a protein target for which binding is available ([de Azevedo et al., 2024](https://doi.org/10.1002/jcc.27449)). It employs a requests library for downloading the atomic coordinates from the RCSB ([Veit-Acosta & de Azevedo, 2021](https://doi.org/10.2174/0929867328666210210121320)).
<br><a href="https://colab.research.google.com/drive/1oKMThoHQ63jB2k6IpjrLccNKo5bOgJ8_?usp" title = "Link to Google Colab">
<img src="https://drive.usercontent.google.com/download?id=1WZ2ekqOvOilsl-zJAZjjw3MRVxvkqSzp&export=view&authuser=0" width=180 alt="Link to Google Colab" ></a><br>
<br> </br>
<img src="https://drive.usercontent.google.com/download?id=1SpdLWV1K6Qtv0kvnRqdc3jc25mL0Vol_&export=view&authuser=0" width=600 alt="DnldTool4RCSB Flowchart">
<br><i>Schematic flowchart for DnldTool4RCSB. It reads input files (lig.in, par.in, and pdb_codes.in) and downloads PDB and SDF from the Protein Data Bank for which binding affinity data (e.g., K<sub>i</sub>) is available. DnldTool4RCSB reads pdb_codes.in to define the PDB file to be downloaded from the Protein Data Bank. Input files lig.in and par.in define the folders used for downloading and the binding affinity. DnldTool4RCSB also downloads the SDF for the active ligand in the structure.</i></br>
<br> </br>
This code has the following functions

**ISO80000**: This function determines the file size in kibibytes (KiB), mebibytes (MiB), gibibytes (GiB) etc. It employs ISO/IEC 80000 standard
(https://www.iso.org/standard/87648.html).
<br> </br>
**read_dictionary**: This function reads a file with parameters stored as Python dictionaries.
<br> </br>
**read_pdb_codes**: This function reads a CSV file with PDB access codes and returns a list with them. It shows a summmary.
<br> </br>
**read_pdb_codes_no_summary**: This function reads a CSV file with PDB access codes and returns a list with them.
<br> </br>
**show_line**: This function shows a formatted line.
<br> </br>
**show_references**: This function shows references given as a list.
<br> </br>
**show_title**: This function shows a formatted line as a title.
<br> </br>
**rcsb_download_sdf**: This function downloads a specific ligand from the PDB using
the RCSB Model Server API and saves it as an SD File.
<br> </br>
**scrape_data_rcsb**: This function scrapes data from the RCSB page. It saves it to a file with the identification of the active ligand found in a given structure.
<br> </br>
**extract_pdb_coordinates**: This function extracts coordinates from a downloaded
PDB file. It intends to select target coordinates for docking simulations.
<br> </br>
**rcsb_download_pdb**: This function downloads a PDB file from the RCSB and saves it to a target directory.
<br> </br>
**zip_content_folders**: This function zips datasets folder in the content directory.
<br> </br>
**download_file_from_google_drive**: This function downloads a file from the google drive.
<br> </br>
**get_confirm_token**: This function gets the confirmation token.
<br> </br>
**save_response_content**: This function saves the response content.
<br> </br>
**unzip_a_folder**: This function unzips a previously zipped folder.
<br> </br>
**make_a_dir**: This function makes a directory in the content folder.
<br> </br>
<br> </br>
Requests library docs available at https://requests.readthedocs.io/en/latest/.

To install the requests library, type the following command.

python -m pip install requests
<br> </br>

**References**
<br> </br>
de Azevedo WF Jr, Quiroga R, Villarreal MA, da Silveira NJF, Bitencourt-Ferreira
G, da Silva AD, Veit-Acosta M, Oliveira PR, Tutone M, Biziukova N, Poroikov V, Tarasova O, Baud S. SAnDReS 2.0: Development of machine-learning models to explore the scoring function space. J Comput Chem. 2024;45(27):2333-2346.
[doi:](https://doi.org/10.1002/jcc.27449)
<br> </br>
Veit-Acosta M, de Azevedo Júnior WF. The Impact of Crystallographic Data for the Development of Machine Learning Models to Predict Protein-Ligand Binding Affinity. Curr Med Chem. 2021;28(34):7006-7022.
[doi:](https://doi.org/10.2174/0929867328666210210121320)
