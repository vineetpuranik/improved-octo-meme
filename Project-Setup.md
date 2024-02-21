# Project Setup

## Elastic cluster single node setup
1. Start Docker Desktop
2. Open powershell as an administrator and run the following command
```
docker run -p 9200:9200 -d --name elasticsearch \
  -e "discovery.type=single-node" \
  -e "xpack.security.enabled=false" \
  -e "xpack.security.http.ssl.enabled=false" \
  -e "xpack.license.self_generated.type=trial" \
  docker.elastic.co/elasticsearch/elasticsearch:8.11.0

```
3. Go to http://localhost:9200 and confirm the service is running.


## Python setup
1. Run the following command to make sure Python is installed
```
python3 --version

```
2. Run the following command to install flask
```
pip3 install flask

```

## Project Setup
1. Download the starter kit from https://www.elastic.co/search-labs/tutorials/search-tutorial/starter-project

2. Navigate to the search-tutorial folder. 
3. Following Python best practices, wer are going to create a virtual environment , a private Python environment dedicated to this project. Run the following command
```
python3 -m venv .venv

```
4. Next we will activate the virtual environment using the command below if using Powershell
```
.\.venv\Scripts\activate

```
5. The terminal command prompt will now start diplaying (.venv)
6. Now we will configure our python environment by installing dependent packages that we need
```
pip install -r requirements.txt

```
7.  Finally we should be able to start our application on port 5001 using the command
```
flask run 

```

## Elasticsearch python client setup
1. Install the Elasticsearch python client using the command
```
pip install elasticsearch

```
2. Update the project dependenices in requirements.txt
```
pip freeze > reqiurements.txt

```
