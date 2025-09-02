# Running the Collection Automatically

## Option 1: Run in Postman UI

1. Open the collection in Postman.  
2. Click **Run Collection**.  
3. Configure:  
   - Number of iterations (e.g., 10)  
   - Environment: `MyLocalEnvironment` (if using one)  
4. Click **Run**.

---

## Option 2: Run with Postman CLI (Newman)

If you prefer running tests from the terminal:

```bash
npm install -g newman

newman run MyApiCollection.postman_collection.json \
  --insecure \
  --iteration-count 5 \
  --delay-request 500 \
  --environment MyLocalEnvironment.postman_environment.json
--insecure allows running with self-signed certificates

--delay-request adds a slight delay between requests

pgsql
Copy code
