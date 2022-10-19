pipeline{
    agent any
    stages{
        stage("Maven Build"){
            steps{
                sh "mvn clean package"
            }
        }
        stage("Deploy to Dev"){
            when {
                branch "develop"
            }
            steps{
                echo "deploy to development server"
            }
        }
        stage("Deploy to stage"){
            when {
                branch "stage"
            }
            steps{
                echo "deploy to stage"
            }
        }
        stage("Deploy to prod"){
            when {
                branch "main"
            }
            steps{
                echo "deploy to prod"
            }
        }
    }
}
