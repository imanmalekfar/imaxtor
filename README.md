
testing github
name: Deploy to Server
  push:
    branches
    runs-on: untu-latest
    steps:
    name: Chekout code
      uses: actions/checkout@v3

     name: Deploy to Production
      uses: apploy/ssh-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        key: ${{ secrets.SSH_KEY }
        script://
          cd /var/www
          
          
          
          
        
      
        
          


