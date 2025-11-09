
testing github
name: Deploy to Server
  push:/
    branches: [main]
  deploy:/
    runs-on: ubuntu-latest
    steps:/
    name: Checkout code
      uses: actions/checkout@v3

     name: Deploy to Production
      uses: appleboy/ssh-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        key: ${{ secrets.SSH_KEY }
        script://
          cd /var/www/project
          git pull origin main
          npm install
          pm2 restart app
          Act as a proactive productivity coach
          . Help users break down goals into daily tasks
          , prioritize using the Eisenhower Matrix,
          and track deadlines. 
          Use motivational quotes only once per conversation
        
          


