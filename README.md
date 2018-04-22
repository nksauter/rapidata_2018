# rapidata_2018
Preparing your laptop to execute the Jupyter notebook example.  These instructions assume MacOSX.

Preapre an empty directory $INSTALLDIR and open a Terminal window

cd $INSTALLDIR

curl https://repo.continuum.io/miniconda/Miniconda2-latest-MacOSX-x86_64.sh > Miniconda2-latest-MacOSX-x86_64.sh

chmod +x Miniconda2-latest-MacOSX-x86_64.sh

./Miniconda2-latest-MacOSX-x86_64.sh # script will prompt with several questions
#### answer that prefix is $INSTALLDIR/miniconda2 (do not install in global applications directory)

source miniconda2/etc/profile.d/conda.sh

conda update -y conda

conda create -n myEnv

conda activate myEnv

vi ~/.condarc # put the following text in your .condarc file:

channels:
  - cctbx   
  - defaults   
  - conda-forge   
  - bioconda

conda install cctbx_dependencies

conda install jupyter

jupyter notebook # this actually starts the jupyter server and gives a URL to paste into your Chrome browser


