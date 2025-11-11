# Data-Science Docker Stack

One-command, reproducible JupyterLab environment with pandas, NumPy, scikit-learn, Matplotlib & Seaborn pre-installed.

## Quick start (macOS / Windows / Linux)

Prerequisites: [Docker Desktop](https://www.docker.com/products/docker-desktop/)

git clone https://github.com/YOUR_GITHUB_USERNAME/ds-docker.git
cd ds-docker
docker compose up

Open http://localhost:8888/lab?token=jl123 in your browser.  
Put notebooks in the notebooks/ folder—they are instantly saved on your host.

## Rebuild the image (optional)

After editing requirements.txt or the Dockerfile:

docker compose build --no-cache
docker compose up

## Structure

.
├── Dockerfile               # Image definition
├── docker-compose.yml      # Service orchestration
├── requirements.txt        # Python libraries
├── notebooks/              # Your work lives here (git-ignored checkpoints)
└── README.md

## Token

Default access token is ds123.  
Change it in docker-compose.yml under --NotebookApp.token='your-new-token'.

## License

MIT (feel free to use for any project).

## AI snapshot

`repomix-output.txt` is an auto-generated, LLM-friendly bundle of the whole repo.  
Regenerate: `npm install -g repomix && repomix`
