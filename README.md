# APIproject

### poetry
```
poetry install
```

```
poetry shell
```

```
# this to run server
poetry run uvicorn backend.main:app --reload
```

```
# main.py
import uvicorn
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}

def start():
    uvicorn.run("backend.main:app", host="0.0.0.0", port=8000, reload=True, workers=2)
```
