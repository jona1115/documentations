```
Create new environment:
conda create -n "name_of_env"
conda create -n "trans2" python=3.11

Activate environment:
conda activate name_of_env

Deactivate:
conda deactivate

See all conda env:
conda env list

Delete env:
conda env remove --name xxx

Export env:
conda env export > environment.yml

Recreate env:
conda env create -f environment.yml
```
