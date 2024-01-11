# python-api
# Getting Started with Python and VS Code

Follow these steps to set up your Python development environment and install Visual Studio Code (VS Code).

## Step 1: Install Python 3

1. Download and install Python 3 from the official website: [Python Downloads](https://www.python.org/downloads/)

2. Once the installation is complete, you can verify that Python 3 is installed by opening your terminal and running the following command:

    ```bash
    python3 --version
    ```

   You should see the Python 3 version displayed.

## Step 2: Check pip3 Version

1. In your terminal, check the version of `pip3` (Python package manager) by running:

    ```bash
    pip3 --version
    ```

   You should see the `pip3` version displayed.

## Step 3: Download and Install VS Code

1. Download Visual Studio Code (VS Code) from the official website: [VS Code Downloads](https://code.visualstudio.com/download)

2. Follow the installation instructions for your operating system.

   - For Windows, run the installer and follow the setup wizard.
   - For macOS, drag and drop VS Code to the Applications folder.
   - For Linux, follow the distribution-specific installation instructions.

Now you're all set up to start coding with Python using VS Code!


create virtual env `python3 -m venv venv`
Activate: `source venv/bin/activate`
Install FastAPI `pip install "fastapi[all]"`
Check all packages installed `pip freeze`
Run the live server: `uvicorn main:app --reload`
Main.py is the entry point of our application
Open `http://127.0.0.1:8000/`
Interactive API docs Now go to `http://127.0.0.1:8000/docs`
Alternative API docs: `http://127.0.0.1:8000/redoc`
Check schema `http://127.0.0.1:8000/openapi.json`

Below is route, A "path" / is also commonly called an "endpoint" or a "route". 
The @app.get("/") tells FastAPI that the function right below is in charge of handling requests that go to:
Instance `app` = FastAPI()
Decorator `@app`.get("/")
http method is @app.`get`("/")
Function name async def `root`(): you can chnage root to a descriptive function name to whatever, like login_user

```bash
app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello Welcome To Python3"}
```

![Alt text](images/FastAPI.png?raw=true "FastAPI")
