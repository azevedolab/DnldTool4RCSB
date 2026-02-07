<H1>DnldTool4RCSB: Download Tool for RCSB</H1>
<a href="https://colab.research.google.com/drive/1oKMThoHQ63jB2k6IpjrLccNKo5bOgJ8_?usp" title = "Link to Google Colab">
<img src="https://drive.usercontent.google.com/download?id=1KdXA4TI3bdnMiXc-dzU99u6s7uMVPgTD&export=view&authuser=0" height=24 alt="Link to Google Colab"></a>  
<a href="https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/dnldtool4rcsb.ipynb" title = "Link to Jupyter Notebook">
<img src="https://drive.usercontent.google.com/download?id=1A4v8xBvC0Na-2Gdi3a5J4l6r0VOki9rK&export=view&authuser=0" height=24 alt="Link to Jupyter Notebook"></a>

This Jupyter Notebook (<a href="https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/dnldtool4rcsb.ipynb" title="Link to Jupyter Notebook">dnldtool4rcsb.ipynb</a>) downloads files (PDB and SDF) with atomic coordinates from the Protein Data Bank. It reads the HTML RCSB page to scrape data related to the identification of the active ligand. It focuses on structures for which binding affinity data is available. The active ligand is a small molecule bound to a protein target for which binding is available ([de Azevedo et al., 2024](https://doi.org/10.1002/jcc.27449)). It employs the [Requests HTTP library](https://requests.readthedocs.io/en/latest/) for downloading the atomic coordinates from the RCSB ([Veit-Acosta & de Azevedo, 2021](https://doi.org/10.2174/0929867328666210210121320)).
<br> </br>
<img src="https://drive.usercontent.google.com/download?id=1SpdLWV1K6Qtv0kvnRqdc3jc25mL0Vol_&export=view&authuser=0" width=400 alt="DnldTool4RCSB Flowchart">
<P>
<i>Schematic flowchart for DnldTool4RCSB. It reads input files (<a href = "https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/lig.in" title = "DnldTool4RCSB Input File">lig.in</a> and <a href = "https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/par.in" title = "DnldTool4RCSB Input File">par.in</a>) and downloads PDB and SDF from the <a href = "https://www.rcsb.org/" Title = "Link to Protein Data Bank">Protein Data Bank</a> for which binding affinity data (e.g., K<sub>i</sub>) is available. DnldTool4RCSB reads <a href = "https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/pdb_codes.in" title = "PDB Codes for Downloading">pdb_codes.in</a> to define the PDB file(s) to be downloaded from the <a href = "https://www.rcsb.org/" Title = "Link to Protein Data Bank">Protein Data Bank</a>. Input files <a href = "https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/lig.in" title = "DnldTool4RCSB Input File">lig.in</a> and <a href = "https://github.com/azevedolab/DnldTool4RCSB/blob/main/src/par.in" title = "DnldTool4RCSB Input File">par.in</a> define the folders used for downloading structures and the binding affinity. DnldTool4RCSB also downloads the SDF for the active ligand in the structure.</i></P>
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
Requests HTTP library docs available at https://requests.readthedocs.io/en/latest/.

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
<br> </br>
<H2>Additional Material Related to DnldTool4RCSB</H2>
<a href = "https://doi.org/10.1007/978-1-0716-4949-7" title = "de Azevedo WF Jr, editor. Docking screens for drug discovery. 2nd ed. New York, NY: Springer; 2026.">
<img src="https://drive.usercontent.google.com/download?id=1qWkaR3YMBMcfofbC9uYrq-gSfsR1BTjx&export=view&authuser=0" width=200 align=left title="de Azevedo WF Jr, editor. Docking screens for drug discovery. 2nd ed. New York, NY: Springer; 2026.">
</a>
<p>
de Azevedo WF Jr, editor. Docking screens for drug discovery. 2nd ed. New York, NY: Springer; 2026. <a href = "https://doi.org/10.1007/978-1-0716-4949-7" title = "de Azevedo WF Jr, editor. Docking screens for drug discovery. 2nd ed. New York, NY: Springer; 2026.">DOI: 10.1007/978-1-0716-4949-7</a>
</p>
<a href="https://www.amazon.com/Docking-Screens-Discovery-Methods-Molecular-ebook/dp/B0FVTT27Z9">
<img src="https://drive.usercontent.google.com/download?id=1ktGUzRY-SOoRjdvc6xKzzBNXzB6ibJfc&export=view&authuser=0" width=100 align=left title="de Azevedo WF Jr, editor. Docking screens for drug discovery. 2nd ed. New York, NY: Springer; 2026.">
</a>
<br> </br>
<br> </br>
<br> </br>
<br> </br>
<br> </br>
<h2>Prof. Dr. Walter F. de Azevedo, Jr.</h2>
<img src="https://drive.usercontent.google.com/download?id=1ao9REI0b_bCbjDy2pu4k3Tbr35LCB5Qt&export=view&authuser=0" width=200 align=left title="Walter Filgueira de Azevedo, Jr. October 02, 2024. Alfenas-MG. Brazil."></a>
<p>
My scientific interests are interdisciplinary, with three main emphases: <a href = "https://doi.org/10.3390/molecules24030637" title = "Nussinov R, Tsai CJ, Shehu A, Jang H. Computational Structural Biology: Successes, Future Directions, and Challenges. Molecules. 2019 Feb 12;24(3):637. doi: 10.3390/molecules24030637">computational structural biology</a>, <a href = "https://www.ibm.com/topics/artificial-intelligence" title = "What is AI?">artificial intelligence</a>, and <a href = "http://www.scholarpedia.org/article/Complex_systems" title = "Complex systems">complex systems</a>. In my studies, I developed several free software programs to explore the concept of <a href = "https://www.eurekaselect.com/article/84362" title = "Heck GS, Pintro VO, Pereira RR, de Ávila MB, Levin NMB, de Azevedo WF. Supervised Machine Learning Methods Applied to Predict Ligand- Binding Affinity. Curr Med Chem. 2017;24(23):2459-2470.">Scoring Function Space</a>. </p>
<p>
As a result of my research, I published over 200 scientific works about protein structures, computer models of complex systems, and simulations of protein systems. These publications have generated over 12,000 citations on <a href = "https://scholar.google.com/citations?user=HWwJXJUAAAAJ&hl=pt-BR" title = "Link to Google Scholar">Google Scholar (h-index of 63)</a> and more than 10,000 citations and an <a href = "https://www.scopus.com/authid/detail.uri?authorId=7006435557" title = "de Azevedo Junior, Walter Filgueira. Scopus ID: 7006435557">h-index of 58 in Scopus</a>.   

Due to the impact of my work, I have been ranked among the most influential researchers in the world (Fields: Biophysics, Biochemistry & Molecular Biology, and Biomedical Research) according to a database created by <a href = "https://pubmed.ncbi.nlm.nih.gov/33064726/" title = "Ioannidis JPA, Boyack KW, Baas J. Updated science-wide author databases of standardized citation indicators. PLoS Biol. 2020 Oct 16;18(10):e3000918. doi: 10.1371/journal.pbio.3000918. PMID: 33064726; PMCID: PMC7567353.">Journal Plos Biology</a> (see news <a href = "https://www.pucrs.br/en/blog/research-database-includes-7-pucrs-professors-among-most-influential-in-the-world/" title = "Research database includes 7 PUCRS professors among most influential in the world">here</a>). The application of the same set of metrics recognized the influence of my work from 2021 to 2025 (<a href = "https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/3" title = "August 2021 data-update for Updated science-wide author databases of standardized citation indicators">Baas et al., 2021</a>; <a href = "https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/4" title = "September 2022 data-update for Updated science-wide author databases of standardized citation indicators">Ioannidis, 2022</a>, <a href = "https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/6" title = "October 2023 data-update for Updated science-wide author databases of standardized citation indicators">2023</a>, <a href = "https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/7" title = "August 2024 data-update for Updated science-wide author databases of standardized citation indicators">2024</a>, and <a href = "https://elsevier.digitalcommonsdata.com/datasets/btchxktzyw/8" title = "August 2025 data-update for Updated science-wide author databases of standardized citation indicators">2025</a>). Not bad for a poor guy who was a shoe seller at a store in São Paulo and had the opportunity to study at the University of São Paulo with a scholarship for food and housing. I was 23 when I initiated my undergraduate studies and was the first in my family to have access to higher education.
<br> </br>
<a href="https://www.scopus.com/authid/detail.uri?authorId=7006435557" title = "Link to Scopus">
<img src="https://drive.usercontent.google.com/download?id=1K_1skqZBcdmgJK41OJJcr4hbXepXHje_&export=view&authuser=0" width=800 alt="Link to Scopus"></a>  
<br><i>Document and Citation Trends (<a href="https://www.scopus.com/authid/detail.uri?authorId=7006435557" title = "Link to Scopus">Scopus ID: 7006435557</a>) (Data captured on January 30, 2026)</i></br>
<br> </br>
Regarding scientific impact (<a href = "https://www.sciencenews.org/article/rating-researchers" title = "Rating Researchers">Peterson, 2005</a>), Hirsch said that for a physicist, an h-index of 45 or higher could mean membership in the National Academy of Sciences of the USA. So far, there have been no invitations. No hard feelings because I am in good company. <a href = "https://theconversation.com/carl-sagans-scientific-legacy-extends-far-beyond-cosmos-240885" title = "Carl Sagan’s scientific legacy extends far beyond ‘Cosmos’">Carl Sagan</a> was never allowed into the National Academy of Sciences. According to an analysis of citations performed on Nov. 9, 2024 (<a href = "https://theconversation.com/carl-sagans-scientific-legacy-extends-far-beyond-cosmos-240885" title = "Carl Sagan’s scientific legacy extends far beyond ‘Cosmos’">The Conversation</a>), his work accumulates more than 1,000 citations per year on Google Scholar. Indeed, his current citation rate exceeds that of many members of the <a href = "https://www.nasonline.org/membership/" title = "National Academy of Sciences">National Academy of Sciences</a>. 

I will continue working in science with low-budget and interdisciplinary projects and combating <a href = "https://revistapesquisa.fapesp.br/en/the-seeds-of-mistrust/" title = "The seeds of mistrust: A new dictionary focuses on the varieties of denialism that confuse public opinion in Brazil and around the world. Ana Paula Orlandi, da Revista Pesquisa FAPESP">denialism</a> with science. The fight against <a href = "https://revistapesquisa.fapesp.br/en/the-seeds-of-mistrust/" title = "The seeds of mistrust: A new dictionary focuses on the varieties of denialism that confuse public opinion in Brazil and around the world. Ana Paula Orlandi, da Revista Pesquisa FAPESP">denialism</a> is a continuing work, and scientists should not forget their role in a complex society where social media has given the right to speak to legions of imbeciles.

“Social media gives the right to speak to legions of imbeciles who previously only spoke at the bar after a glass of wine, without damaging the community. They were immediately silenced, but now they have the same right to speak as a Nobel Prize winner. It’s the invasion of imbeciles.”

Umberto Eco. Source: <a href = "https://quoteinvestigator.com/2024/03/21/social-media/" title = "Quote Origin: Social Media Gives the Right To Speak To Legions of Imbeciles Who Previously Only Spoke in Bars After Drinking">Quote Investigator</a>
</p>
<br> </br>
"Let the light of science end the darkness of denialism." My quote (<a href = "https://doi.org/10.2174/092986732838211207154549" title = "DOI:10.2174/092986732838211207154549">DOI:10.2174/092986732838211207154549</a>). 
<br> </br>
