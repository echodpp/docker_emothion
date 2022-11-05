* packages
pip install transformers==4.22.2 && \
pip install torch==1.12.1+cpu --extra-index-url https://download.pytorch.org/whl/cpu

* build docker
docker build -t echodpp/bert-base-uncased-emotion:2022.09.30 -f docker/bert-base-uncased-emotion/Dockerfile .

* test with:
docker run --rm -it echodpp/bert-base-uncased-emotion:2022.09.30
