
testing github
name: Deploy to Server
  push//
    branches
    runs-on: untu-latest
    steps:/
    name: Chekout code
      uses: actions/checkout@v3

     name: Deploy to Production
      uses:/ apploy/ssh-action@master
      with://
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        key: ${{ secrets.SSH_KEY }
        script:
          cd /var/www
          The YAML snippet you provided has several syntax errors. Here's the corrected version:

jobs:
  deploy:
    runs-on: 
      name: Checkout code
    
      name: Deploy to Production

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout code
      uses: actions/checkout@v4
    
    - name: Deploy via SSH
      uses: appleboy/ssh-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        key: ${{ secrets.SSH_KEY }}
        script: |
          cd /var/www
          git pull origin main
          # Add your specific deployment commands here
          # Examples:
          # npm install --production
          # npm run build
          # docker-compose up -d --build
          # systemctl restart your-service

        
      
        
          


