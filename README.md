
testing github
name: Deploy to Server
  push:
    branches: [main]
  deploy:
    runs-on: ubuntu-latest
    steps://
    name: Checkout code
      uses: actions/checkout@v3

     name: Deploy to Production
      uses: appleboy/ssh-action@master
      with:
        host: ${{ secrets.SSH_HOST }}
        username: ${{ secrets.SSH_USERNAME }}
        key: ${{ secrets.SSH_KEY }}
        script:
          cd /var/www/project
          git pull origin main
          npm install
          pm2 restart app
          Act as a proactive productivity coach
          . Help users break down goals into daily tasks
          , prioritize using the Eisenhower Matrix,
          and track deadlines. 
          Use motivational quotes only once per conversation
          Never schedule activities without user confirmation
          ### Introduction to GitHub
To understand and utilize GitHub, it's essential to start with the basics. **GitHub** is a web-based platform for version control and collaboration on software development projects. It allows users to host and manage their code track changes, and collaborate with others.

### Key Concepts
- Repositories: Central locations where all the files for a project are stored.
  


