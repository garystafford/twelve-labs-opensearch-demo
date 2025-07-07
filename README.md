# Multi-Vector Semantic Search: Advanced Video Search with TwelveLabs and Amazon OpenSearch

Code for the Medium blog post, [Multi-Vector Semantic Search: Advanced Video Search with TwelveLabs and Amazon OpenSearch](https://garystafford.medium.com/multi-vector-semantic-search-advanced-video-search-with-twelve-labs-and-amazon-opensearch-7b81ba52c373), also on [LinkedIn](https://www.linkedin.com/pulse/multi-vector-semantic-search-advanced-video-twelve-labs-gary-stafford-dmjoc/?trackingId=H5lUSIgrTv6eBGlnmr%2Fo6g%3D%3D). How TwelveLabs AI Models and Amazon OpenSearch Serverless enable multi-vector semantic and hybrid search for video content.

![Architecture](twelve_labs_bedrock.png)

## Prerequisites

- Python 3.12+
- AWS credentials
- Amazon OpenSearch Serverless collection
- TwelveLabs API key

## Installation

### Clone the repository

```bash
git clone https://github.com/garystafford/twelve-labs-opensearch-demo.git
cd twelve-labs-opensearch-demo
```

### Rename `python-dotenv` file:

Mac:

```bash
mv env.txt .env
```

Windows:

```bat
rename env.txt .env
```

### Create the required directories

Mac:

```bash
mkdir -p "videos/pexels"
mkdir -p "output/pexels"
mkdir -p "documents/pexels"
```

Windows:

```bat
mkdir "videos\pexels"
mkdir "output\pexels"
mkdir "documents\pexels"
```

### Create a Python virtual environment for the Jupyter Notebook:

Mac:

```bash
python -m pip install virtualenv -Uq
python -m venv .venv
source .venv/bin/activate
```

Windows:

```bat
python -m venv .venv
.venv\Scripts\activate
```

## Run the Code

Access the Jupyter Notebook for all the code:

[twelve-labs-demo-nested-public.ipynb](twelve-labs-demo-nested-public.ipynb)

## Alternative: Running OpenSearch in Docker

As an alternative to AWS, you can run OpenSearch locally using Docker. This is insecure and intended only for development environments.

Mac:

```bash
docker swarm init

SWARM_ID=$(docker node ls --format "{{.ID}}")
docker stack deploy -c docker-compose.yml $SWARM_ID

docker service ls
```

Windows:

```bat
docker swarm init

for /f "delims=" %x in ('docker node ls --format "{{.ID}}"') do set SWARM_ID=%x
docker stack deploy -c docker-compose.yml %SWARM_ID%

docker service ls
```

---

_The contents of this repository represent my viewpoints and not those of my past or current employers, including Amazon Web Services (AWS). All third-party libraries, modules, plugins, and SDKs are the property of their respective owners._
