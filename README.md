# VCC_Assignment-1
Setup & Deployment

**1.** Update System
sudo apt update

**2️.** Install Node.js and npm
sudo apt install -y nodejs npm


Verify installation:

node -v
npm -v

**3️.** Create Project Directory
mkdir microservice
cd microservice

**4️.** Initialize Node.js Project
npm init -y

**5️.** Install Dependencies
npm install express

**6️.** Create Application (app.js)

**7️.** Start the Microservice
node app.js


Service will run on port 3000.
 Testing the API
 Test on VM-1 (Local)
Install curl if needed:
sudo apt-get install curl
curl http://localhost:3000/api/hello

**Expected output:**

{
  "message": "Hello from VM-1"
}

Test from VM-2 (Remote)
Use VM-1’s IP address:
curl http://<VM-1-IP>:3000/api/hello


Expected output:
{
  "message": "Hello from VM-1"
}

**Network Configuration:**

Both VMs must be connected to the same NAT Network

VM-1 must expose port 3000

IP address of VM-1 should be reachable from VM-2

 **Result:**

Microservice successfully deployed on VM-1

API accessed from VM-2

Inter-VM communication verified
