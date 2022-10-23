# docker_emothion

## Source
bert-base-uncased-emotion model can be found here at [hugging face](https://huggingface.co/bhadresh-savani/bert-base-uncased-emotion?text=I+like+you.+I+love+you)
## Packages
* transformers 
* torch
```
pip install transformers==4.22.2 && \
pip install torch==1.12.1+cpu --extra-index-url https://download.pytorch.org/whl/cpu
```
test model with example main.py:
```
from transformers import pipeline
classifier = pipeline("text-classification",model='bhadresh-savani/bert-base-uncased-emotion', top_k=1)
prediction = classifier("Good Good Study, Day Day Up", )
print(prediction)
```
python main.py
```
docker build -t echodpp/bert-base-uncased:2022.09.30 -f docker/bert-base-emotion/Dockerfile .
```
docker run 
```
[[{'label': 'joy', 'score': 0.994911253452301}]]
```
