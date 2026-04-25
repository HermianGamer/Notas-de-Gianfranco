1. Add the `pygame` [[Python Library]] as a project dependency:
    
    ```sh
    uv add pygame==2.6.1
    ```
    
    This tells Python that this [[Project]] requires `pygame` with an exact version of `2.6.1`.
    
2. Make sure `pygame` is installed:
    
    ```sh
    uv run -m pygame
    ```
    

This will **result in an error** (the test expects an exit code of 1), but the output will show that `pygame` is installed.