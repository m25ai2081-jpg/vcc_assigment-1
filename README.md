# vcc_assigment-1
Setup & Deployment

1️⃣ Update System
sudo apt update

2️⃣ Install Node.js and npm
sudo apt install -y nodejs npm


Verify installation:

node -v
npm -v

3️⃣ Create Project Directory
mkdir microservice
cd microservice

4️⃣ Initialize Node.js Project
npm init -y

5️⃣ Install Dependencies
npm install express

6️⃣ Create Application (app.js)

7️⃣ Start the Microservice
node app.js


Service will run on port 3000.

🧪 Testing the API
✅ Test on VM-1 (Local)

Install curl if needed:

sudo apt-get install curl

curl http://localhost:3000/api/hello


Expected output:

{
  "message": "Hello from VM-1"
}

🌐 Test from VM-2 (Remote)

Use VM-1’s IP address:

curl http://<VM-1-IP>:3000/api/hello


Expected output:

{
  "message": "Hello from VM-1"
}

🌐 Network Configuration

Both VMs must be connected to the same NAT Network

VM-1 must expose port 3000

IP address of VM-1 should be reachable from VM-2

✅ Result

Microservice successfully deployed on VM-1

API accessed from VM-2

Inter-VM communication verified
