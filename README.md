## SommAI

### Wine recommender based on Natural Language Processing and Machine Learning

### Dataset: professional wine reviews scraped from WineEnthusiast available on Kaggle:
 - WineEnthusiast source: https://www.winemag.com/?s=&drink_type=wine
 - KAGGLE source: https://www.kaggle.com/zynicide/wine-reviews

### Extra info:
 - WineFolly: https://winefolly.com/


### Build docker image to run the notebook

```
docker build -t sommai_img .
```

### Run notebook server in docker

```bash
docker run -it --rm \
    -p 8888:8888 \
    -v $(pwd)/notebooks:/home/jovyan/notebooks \
    -v $(pwd)/data:/data/ \
    -v $(pwd)/images:/images/ \
    sommai_img \
    jupyter notebook --notebook-dir /home/jovyan/notebooks
```
