Deploying my-app with Kubernetes locally

Step 1: Build image
- navigate to my-app dir (where Dockerfile is present)
- run
    - docker build -t my-app:1.2 .

Step 2: Prerequists
- Ensure Ingress controller is installed
    - https://kubernetes.github.io/ingress-nginx/deploy/
- Include my-app.com in hosts file of local machine

Step 3: Run manifests
- navigate to manifests dir
- run
    - kubectl apply -f .

Step 4: Access applications:
- my-app: http://my-app.com
- mongo express: http://localhost:30001

---

To stop & delete entire env:
- navigate to manifets dir
- run
    - kubectl delete -f .

