# TuChisteDiario

## Python env installation

### Ubuntu:

```
sudo apt install ffmpeg
sudo apt install python3.10-venv
python3.10 -m venv .env
source .env/bin/activate
pip install -r requirements.txt
```

Then, select .env in notebooks Bark.ipynb and createSubtitles.ipynb

To use SadTalker we need python3.8:

```
sudo apt install python3.8-venv
python3.8 -m venv .env_sadtalker
source .env_sadtalker/bin/activate
pip install -r requirements.txt
pip install ipywidgets
```

install in ubuntu:

```
sudo apt-get update
sudo apt install software-properties-common
git clone https://github.com/Winfredy/SadTalker
```

If you have an error cloning SadTalker, you could have to execute:

```
git config --global http.postBuffer 524288000
```