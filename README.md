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
└── twelve-labs-demo-nested-public.ipynb  # All code for blog post demonstration

```

## Usage Instructions

### Prerequisites

- Python 3.7+
- AWS credentials
- Amazon OpenSearch Collection
- Twelve Labs API key

### Installation

Clone the repository:

```bash
git clone https://github.com/garystafford/twelve-labs-opensearch-demo.git
cd twelve-labs-opensearch-demo
```

---

_The contents of this repository represent my viewpoints and not those of my past or current employers, including Amazon Web Services (AWS). All third-party libraries, modules, plugins, and SDKs are the property of their respective owners._
