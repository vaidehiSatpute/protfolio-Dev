pipeline {
    agent any 
    
    stages{
        stage("Clone Code"){
            steps {
                echo "Cloning the code"
                git url:"https://github.com/rajatrokde/protfolio-Dev.git", branch: "master"
            }
        
        }
        stage("Build"){
            steps {
                echo "Building the image"
                sh 'docker build -t mywebsites .' 
            }
        }
        stage("Deploy"){
            steps {
                echo "Deploying the container"
                sh "docker-compose down && docker-compose up -d"
                
            }
        }
        
        stage("Push to Docker Hub"){
            steps {
                echo "Pushing the image to docker hub"
               
                }
            }
    }
    
}
