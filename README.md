# ml_duplicate_claim

project setup

Step 1 — Clone the repo:
git clone <your-repo-url>
cd ml_duplicate_claim



Step 2 — Create virtual environment:
cd api
python3 -m venv venv
source venv/bin/activate


Step 3 — Install dependencies:
pip install fastapi uvicorn sentence-transformers scikit-learn pandas numpy


Step 4 — Generate embeddings:
cd ../model
../api/venv/bin/python train_model.py


Step 5 — Run the server:
cd ../api
uvicorn server:app --reload




train model ===> python train_model.py (/model directory)

now run api ===> python -m uvicorn server:app --reload (/api directory)

for duplicate claims 

# Duplicate of claim 1 (Car accident)
curl "http://localhost:8000/check?text=Automobile%20accident%20on%20highway%20front%20bumper%20damaged"

# Duplicate of claim 2 (Medical)
curl "http://localhost:8000/check?text=Hospital%20treatment%20for%20fractured%20arm%20surgery"

# Duplicate of claim 3 (Flood)
curl "http://localhost:8000/check?text=Heavy%20rain%20caused%20flooding%20in%20home%20basement"

# Duplicate of claim 4 (Car theft)
curl "http://localhost:8000/check?text=Vehicle%20stolen%20from%20parking%20area%20overnight"
