# reproducibility-tutorial
tutorial at https://learning.cyverse.org/projects/cyverse-cyverse-reproducbility-tutorial/en/latest/index.html

### install miniconda, a minimal conda install:
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
```

### create symbolic links within atmosphere session:
```
ln -s /opt/conda/pkgs/*/bin/* /bin
ln -s /opt/conda/pkgs/*/lib/* /usr/lib
```

### install jupyter notebook, nodejs, and necessary kernals
```
/opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
/opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
/opt/conda/bin/pip install bash_kernel
/opt/conda/bin/pip install ipykernel
/opt/conda/bin/python3 -m bash_kernel.install
```

### install snakemake 5.8.1.
```
/opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1

ln -s /opt/conda/bin/* /bin
ln -s /opt/conda/lib/* /usr/lib

snakemake --version
```

### install docker
```
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get update
```

### install and test docker
```
sudo apt-get install -y docker-ce docker-ce-cli containerd.io

docker run hello-world
```

 
# stopped at 'Setup your local filesystem'
