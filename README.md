# Multi-Vector Semantic Search: Advanced Video Search with TwelveLabs and Amazon OpenSearch

Code for the Medium blog post, [Multi-Vector Semantic Search: Advanced Video Search with TwelveLabs and Amazon OpenSearch](https://garystafford.medium.com/multi-vector-semantic-search-advanced-video-search-with-twelve-labs-and-amazon-opensearch-7b81ba52c373), also on [LinkedIn](https://www.linkedin.com/pulse/multi-vector-semantic-search-advanced-video-twelve-labs-gary-stafford-dmjoc/?trackingId=H5lUSIgrTv6eBGlnmr%2Fo6g%3D%3D). How TwelveLabs AI Models and Amazon OpenSearch Serverless enable multi-vector semantic and hybrid search for video content.

![Architecture](twelve_labs_bedrock.png)

## Repository Structure

```text
.
├── documents/                            # OpenSearch documents
│   ├── pexels/
├── output/                               # Generated analyses and embeddings
│   ├── pexels/
├── videos/                               # Source videos
│   ├── pexels/
├── sample_document.json                  # Sample OpenSearch document
└── twelve-labs-demo-nested-public.ipynb  # All code for blog post demonstration
```

## Usage Instructions

### Prerequisites

- Python 3.12+
- AWS credentials
- Amazon OpenSearch Serverless collection
- TwelveLabs API key

The Notebook will require the following environment variables:

```bash
# AWS Credentials (or modify code to use alternative authentication method)
AWS_REGION=<Your AWS Region>
AWS_ACCESS_KEY_ID=<Your AWS Access Key ID>
AWS_SECRET_ACCESS_KEY=<Your AWS Secret Access Key>
AWS_SESSION_TOKEN=<Your AWS Session Token>

# TwelveLabs' API Key
TL_API_KEY=<Your TL API Key>

# OpenSearch endpoint without 'http://' prefix
OPENSEARCH_ENDPOINT=<Your OpenSearch Endpoint>
```

### Installation

Clone the repository and create the required directories:

```bash
git clone https://github.com/garystafford/twelve-labs-opensearch-demo.git
cd twelve-labs-opensearch-demo

mkdir -p "videos/pexels"
mkdir -p "output/pexels"
mkdir -p "documents/pexels"
```

Create a Python virtual environment for the Jupyter Notebook:

```bash
python -m pip install virtualenv -Uq
python -m venv .venv
source .venv/bin/activate
```

### Run the Code

Access the Jupyter Notebook for all code:

[twelve-labs-demo-nested-public.ipynb](twelve-labs-demo-nested-public.ipynb)

---

_The contents of this repository represent my viewpoints and not those of my past or current employers, including Amazon Web Services (AWS). All third-party libraries, modules, plugins, and SDKs are the property of their respective owners._
