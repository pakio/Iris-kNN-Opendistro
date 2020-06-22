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

# check result with Kibana
1. Open Kibana 
Access "localhost:5601"

default id and password is
```
ID : admin
PS : admin
```

2. Open dev tools

3. query for the result
```
GET /iris/_search
{
  "size": 1,
  "query": {
    "knn": {
      "my_vector": {
        "vector": [
          0,
          1
        ],
        "k": 1
      }
    }
  }
}
```

