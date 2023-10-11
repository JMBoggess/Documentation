# VSCode Debugging
Using Visual Studio Code to debugg Azure Web App written in Python using Flask

## Conda Environment
The Conda Environment activated by the debugger is based on the python interpreter selected, to modify:
- Ctrl + Shift + P (or View > Command Pallet)
- Search for - Python: Select Interpreter
- Select the appropriate Python in the conda environment for your web app

## Port 5000
By default, the Flask app will run on port 5000. This may be used by another Windows process.

Error: An attempt was made to access a socket in a way forbidden by its access permissions

You can specify a different port in the launch.json file, for example:

```json
{
   "configurations": [
      {
         "args": [
            "run"
            "--no-reload",
            "--port","5001"
         ]
      }
   ]
}
```
