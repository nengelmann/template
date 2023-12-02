# Developers and maintainers readme

## Additional installation
```bash
source .venv/bin/activate
```

```bash
python -m pip install pip-tools
python -m pip install debugpy
```

## Update the requirements
```bash
rm requirements.txt
python -m piptools compile
```

## Debug with CLI arguments
```bash
python -m debugpy --listen 5678 --wait-for-client src/meetingcam/main.py 
```
Then attach with this VSCode configuration:
```json
{
    "name": "Python: Attach",
    "type": "python",
    "request": "attach",
    "connect": {
        "host": "localhost",
        "port": 5678
    }
}
```
See also: https://code.visualstudio.com/docs/python/debugging
