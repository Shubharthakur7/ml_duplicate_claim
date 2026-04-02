# ml_duplicate_claim


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
