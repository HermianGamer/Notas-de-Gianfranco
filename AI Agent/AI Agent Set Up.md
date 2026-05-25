  
Let's set up a virtual environment for our project.

Virtual environments are Python's way to keep dependencies (e.g., the Google AI libraries we're going to use) separate from other projects on our machine.

## Assignment

1. Use `uv` to create a new project. It'll create the directory and also initialize a Git repo in it.
    
    ```sh
    uv init your-project-name
    cd your-project-name
    ```
    
2. Create a virtual environment at the top level of your project directory:
    
    ```sh
    uv venv
    ```
    
    Make sure your virtual environment directory, usually `.venv` or `venv`, is added to your `.gitignore`file.
    
3. Activate the virtual environment:
    
    ```sh
    source .venv/bin/activate
    ```
    
    You should see something like `(your-project-name)` in your terminal prompt; for example, mine is:
    
    ```text
    (aiagent) wagslane@MacBook-Pro-2 aiagent %
    ```
    
    Always make sure your virtual environment is _activated_ when running code or using the Boot.dev CLI in this course.
    
4. Use `uv` to add two dependencies to the project, _with these specific versions_. They will be added to `pyproject.toml`:
    
    ```sh
    uv add google-genai==1.12.1
    uv add python-dotenv==1.1.0
    ```
    
    This tells Python that this project requires [`google-genai`](https://pypi.org/project/google-genai/) version `1.12.1` and [`python-dotenv`](https://pypi.org/project/python-dotenv/) version `1.1.0`.
    

To run the project using the `uv` virtual environment, you can use the following command:

```sh
uv run main.py
```

In your terminal, you should see something like `Hello from YOUR PROJECT NAME`.