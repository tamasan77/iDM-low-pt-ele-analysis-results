# iDM-low-pt-ele-analysis-results
A summary of results for investigating the potentials of using the BParking electron reconstruction algorithm in the search for iDM with MET and low pt electrons (CADI line EXO-020-010). Using xbgoost to come up with a unique id is also being investigated. The currect xgboost file contains a manually fitted model. Optimal parameters could be found using GridSearchCV. 


# Some tutorials and useful links
Physics Forum Presentation:
https://docs.google.com/presentation/d/1xcOoSxzLFKQFWFYETnTiv73Za4Ybk20J_kcXGjIZtFA/edit#slide=id.p

A comparison of samples with CTau = 1mm and 10mm:
https://docs.google.com/document/d/1KCcRDivZm00qpFNL7V8tFb79Cw6fGDpIE8egIrTqf0c/edit

Uproot tutorial: 
https://indico.cern.ch/event/814895/

Allie’s coffea slides: 
https://indico.cern.ch/event/843368/contributions/3540916/attachments/1969108/3276861/ahall_CoffeaIntro_DAS2020.pdf

Columnar analysis: 
https://indico.cern.ch/event/917676/

Coffea benchmarks: 
https://github.com/mat-adamec/coffea-benchmarks/blob/master/benchmarks

Coffea wiki:
https://coffeateam.github.io/coffea/index.html

The other low pt lepton group's github (Dominic and Christian)
https://github.com/therwig/ele-studies

Intro to machine learning: 
https://indico.cern.ch/event/917681/

Great resource for xgboost:
https://www.youtube.com/user/joshstarmer

# A guide on computing

Instructions on the conda environment that we are using: (FireHydrant) (See README.md for a quick guide on getting started)
https://github.com/areinsvo/FireHydrant

Analysis code for SIDM, making use of [Coffea](https://github.com/CoffeaTeam/coffea).

Environment management: [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

Requirements:

- python3
- [Coffea](https://github.com/CoffeaTeam/coffea)
- [xrootd](https://github.com/xrootd/xrootd-python)
- [jupyterlab](https://github.com/jupyterlab/jupyterlab)

---
# Log into LPC
```
ssh -L  8888:localhost:8888 USERNAME@cmslpc-sl7.fnal.gov
```
Replace 8888 with your favourite port.

# Activation/Deactivation

- `conda activate FireHydrant`
- `conda deactivate`

# Start `jupyterlab`

```bash
jupyter lab --no-browser --port=8888 # replace by your favourite port
```

# Setup (@FNAL LPC)

1. Install Miniconda (if you have not install Miniconda yet)

    - go to https://docs.conda.io/en/latest/miniconda.html,
    - get the bash installer script of Linux, Python3.7 64-bit with `wget` or `curl`,
    - then `bash Miniconda3-latest-Linux-x86_64.sh`
    - (you need to type `ENTER` or `yes` at some point, add conda sourcing to your `.bashrc` or equivalent)
    - a quick [reference](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) on managing environments with `conda`.

2. Edit/create .bash_profile file (for Bash users only)
    
    - open `~/.bash_profile` 
    - add the line: `source ~/.bashrc`
    - save and exit

3. Clone repo

    ```bash
    git clone https://github.com/areinsvo/FireHydrant.git
    cd FireHydrant
    ```

4. Install packages

    ```bash
    ./setup.sh
    ```


