pipeline {
    agent any

    stages {
        stage("Clone") {
            steps {
                echo "Cloning the repo"
                git url: "https://github.com/Arjun4522/Simon_GAme.git", branch: "main"
            }
        }
        stage("Build") {
            steps {
                echo "Building the image"
                sh "docker build -t app ."
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying the container"
                sh "docker run -d -p 8000:8000 app:latest"
            }
        }
    }
}
