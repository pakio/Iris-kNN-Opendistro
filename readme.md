# Description
Tutorial for using opendistro for Elasticsearch kNN plugin with Iris Dataset

## requirements
- Docker
- Docker Compose
- python
- pip

## Directory Structure
```
.
├── docker-compose.yml  definition of docker environment
├── notebook            uses for preparing and indexing data
│   └── Iris-kNN.ipynb   
├── readme.md
└── requirements.txt    requirements for the scripts
```

# Get ready for work
## preparing
1. install required software in requuiremtns

2. run pip install to install required libralies
```bash
pip install -r requirements.txt
```

3. Run Docker containers
```bash
docker-compose up -d
```

4. Runu python scripts
```
cd notebook
jupyter notebook
```

after jupyter being ready, Open `Iris-kNN.ipynb` and run all cells.

