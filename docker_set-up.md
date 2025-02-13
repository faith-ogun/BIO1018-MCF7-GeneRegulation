### Quick Docker Commands/Set-Up:

docker build -t "name" -f "Dockerfile.txt" .

docker build -t "get_complete" -f "Dockerfile.txt" .  

On local machine:

---
```bash
docker run --entrypoint /bin/bash -it -v /Users/faith/Desktop/Coding:/home/xf2217 get_complete``

docker run -it -p 8888:8888 -v /Users/faith/Desktop/Coding:/Users/faith/Desktop/Coding  get_complete  jupyter notebook --allow-root --ip 0.0.0.0 --no-browser --NotebookApp.token='' --NotebookApp.password='' --notebook-dir=/Users/faith/Desktop/Coding
```

---
  
With Meluxina:
### *Solution:*

```bash
module load Python/3.11.3-GCCcore-12.3.0 

#If a package doesn't work.
rm -rf /home/users/u102501/.local/lib/python3.12/site-packages/urllib3*
python -m pip install --upgrade --force-reinstall urllib3
python -c "import urllib3; print(urllib3.__version__)"
```

```bash
module load Apptainer/1.3.1-GCCcore-12.3.0 

apptainer exec --bind /project/home/p200469/get_BIO1018 get_complete_latest.sif python -m jupyter lab --no-browser --ip "*" --NotebookApp.token='' --NotebookApp.password='' --notebook-dir /project/home/p200469/get_BIO1018 --port 8888
```

Split terminal screen:

In local machine:

`ssh -L 8888:localhost:8888 u102501@login.lxp.lu -p 8822 -i ~/.ssh/id_ed25519_mlux`

Enter passphrase,

Then,

`ssh -L 8888:localhost:8888 <mel0000>`  swap <> for your node.
