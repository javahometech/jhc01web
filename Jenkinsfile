pipeline{
    agent any
    stages{
        stage("Maven build"){
            steps{
                sh "mvn clean package"
            }
        }
         stage("Deploy to Dev"){
             when {
                 branch "Deveplop to deveplopment server"
             }
            steps{
                echo "deploy"
            }
        }
        stage("Deploy to Stage"){
            when {
                 branch "stage"
             }
            steps{
                echo "deploy to stage"
            }
        }
        stage("Deploy to Prod"){
            when {
                 branch"main"
             }
            steps{
                echo "deploy to prod"
            }
        }
    }
}
