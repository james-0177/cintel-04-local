## cintel-04-local

Module 4 involves local development using tools installed on my own PC. These tools will include:  Python, VS Code, and Git. All of these tools were previously installed on my PC when I took course 44-608 Data Analytics Fundamentals.

# Create and Activate Project Virtual Environment

```shell
py -m venv .venv
.venv\Scripts\Activate
```

# Verify PIP is updated

```shell
py -m pip install --upgrade pip setuptools
```

# Install and update packages from requirements.txt

```shell
py -m pip install --upgrade -r requirements.txt
```

# Freeze requirements

```shell
py -m pip freeze > requirements.txt
```

# Launch app in web browser

```shell
shiny run --reload --launch-browser penguins/app.py
```

# Build Client-Side App

```shell
shiny static-assets remove
shinylive export penguins docs
py -m http.server --directory docs --bind localhost 8008
```

Open web browser (I use Chrome) and navigate to http://localhost:8008

# Update GitHub Repository

```shell
git add .
git commit -m "Update GitHub Repository with local build and shiny commands"
git push -u origin main
```