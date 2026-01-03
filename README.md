
testing github
name: Deploy to Server
  push//
    branches
    runs-on: untu-latest
    steps://
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
    runs-on: ubuntu-latest
    steps:
      name: Checkout code
        uses: actions/checkout@v3

      name: Deploy to Production
        uses: appleboy/ssh-action@master
        with:
          host: ${{ secrets.SSH_HOST }}

Key fixes made:
Fixed indentation (YAML requires consistent 2-space indentation)
Corrected runs-on value to ubuntu-latest
Added proper job structure (jobs: top-level key with job name deploy)
Fixed step syntax (each step starts with -)
Corrected action name to appleboy/ssh-action (was misspelled as "apploy")
Removed invalid comment syntax (// → # for comments)
Fixed with: parameter structure

To use this workflow:
Save it as .github/workflows/deploy.yml
Add these secrets to your repository:
   SSH_HOST (your server IP/hostname)
   SSH_USERNAME (add to with: section)
   SSH_KEY (your SSH private key)

          
        
      
        
          


