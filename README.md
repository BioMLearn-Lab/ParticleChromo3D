------------------------------------------------------------------------------------------------------------------------------------
# ParticleChromo3D -  Particle Swarm Optimization for Chromosome and genome 3D Structure Prediction from Hi-C Data  
------------------------------------------------------------------------------------------------------------------------------------
**OluwadareLab,**
**University of Colorado, Colorado Springs**

----------------------------------------------------------------------
**Developers:** <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;David Vadnais<br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Department of Computer Science <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;University of Colorado, Colorado Springs <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Email: dvadnais@uccs.edu <br /><br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Micheal Middleton<br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Department of Computer Science <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;University of Colorado, Colorado Springs <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Email: mmiddlet@uccs.edu 

**Contact:** <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Oluwatosin Oluwadare, PhD <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Department of Computer Science <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;University of Colorado, Colorado Springs <br />
		 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Email: ooluwada@uccs.edu 
    
--------------------------------------------------------------------	

**1.	Content of folders:**
-----------------------------------------------------------	
src: Python Source Code and utility's used

**2.	Hi-C Data used in this study:**
-----------------------------------------------------------
In our study, we used the synthetic dataset from [Adhikari, et al](https://doi.org/10.1186/s12864-016-3210-4). The contact maps, the original models and their reconstructed models used in this study were downloaded from [here](http://sysbio.rnet.missouri.edu/bdm_download/chromosome3d/unzipped/Input/Synthetic/)

The GM12878 cell Hi-C dataset, GEO Accession number GSE63525, was downloaded from [GSDB](http://sysbio.rnet.missouri.edu/3dgenome/GSDB/details.php?id=GM12878) with GSDB ID: OO7429SF

**3.	Input matrix file format:**
-----------------------------------------------------------

Square Matrix Input format: The square matrix is a space seperated N by N intra-chromosomal contact matrix derived from Hi-C data, where N is the number of equal-sized regions of a chromosome.

**4.	Usage:**
-----------------------------------------------------------

Install env with anaconda from spec-file: <br />
conda create --name ParticleChromo3D --file ParticleChromo3d_env.txt

Or install dependencies individually <br />

<u>Dependencies:</u> <br />
&nbsp;&nbsp;Biopython - 1.7.8 <br />
&nbsp;&nbsp;scipy - 1.5.2 <br />
&nbsp;&nbsp;numpy - 1.19.2 <br />

<u>usage</u>: python3 Ps.py infile [-h] [-sc SWARMCOUNT] [-itt ITTCOUNT] [-t THRESHOLD] [-rr RANDRANGE] <br />
			
<u>positional arguments:</u> <br />
&nbsp;&nbsp;infile  <br />
	&nbsp;&nbsp;&nbsp;&nbsp;Input filed in the format of a matrix of contacts <br />

<u>optional arguments:</u> <br />	
	&nbsp;&nbsp;-h, --help  show this help message and exit<br />
	&nbsp;&nbsp;-sc SWARMCOUNT, --swarmCount SWARMCOUNT <br />
		&nbsp;&nbsp;&nbsp;&nbsp;Number of swarms in system [Default 10] <br />
	&nbsp;&nbsp;-itt ITTCOUNT, --ittCount ITTCOUNT <br />
		&nbsp;&nbsp;&nbsp;&nbsp;Maximum itterations before stop [Default 30000] <br />
	&nbsp;&nbsp;-t THRESHOLD, --threshold THRESHOLD <br />
		&nbsp;&nbsp;&nbsp;&nbsp;Error threshold before stoping [Default 0.000001] <br />	
	&nbsp;&nbsp;-rr RANDRANGE, --randRange RANDRANGE <br />
		&nbsp;&nbsp;&nbsp;&nbsp;Range of x,y,z starting coords. Random value bewtween -randRange,randRange [Default 1] <br />

	
**5.	Output:**
-----------------------------------------------------------
A pdb file and  log file.

