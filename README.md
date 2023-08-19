## What is it? 🧐
A repository for setting up Python development environments on your personal computer using Docker. This allows you to create environments tailored for Python web scraping or using advanced AI tools like Chat GPT.

Designed to work on a MacBook Air with the M2 chip.

## How to Use It? 🧐

### Step 1: Clone the Repository
```
git clone https://github.com/yumelab-imai/python_development_environment_with_docker.git
```

### Step 2: Navigate to the Directory
```
cd python_development_environment_with_docker/
```

### Step 3: Build the Image and Start the Container
```
docker-compose up -d --build
```

### Step 4: Check if the Container Started Successfully
```
docker container ls
```
If successful, you should see an output similar to:
```
CONTAINER ID   IMAGE                COMMAND                 CREATED          STATUS          PORTS                    NAMES
123445        jupyterlab-test-img   "jupyter-lab --ip 0.…"  13 seconds ago   Up 13 seconds   0.0.0.0:6666->6666/tcp   dev-jupyterlab
```

### Step 5: Connect to the Python Environment inside the Container
```
docker-compose exec jupyterlab bash
```

### Step 6: Test the Environment
```
python3 sample.py
```

### To Check JupyterLab Token:
```
docker logs jupyterlab-test | tail
```

## Reference URL
[How to setup Python with Docker](https://www.kagoya.jp/howto/cloud/container/dockerpython/)

## Library Information
| Module        | Purpose                 |
| ------------- | ----------------------- |
| pandas        | CSV Output               |
| requests      | Fetching data |
| BeautifulSoup | HTML Parsing             |
