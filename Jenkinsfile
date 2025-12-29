pipeline{
    agent{
        label 'java-slave'
    }
    stages{
        stage('Build'){
            steps{
                echo "Building the application"
            }

        }
        stage('Scans'){
            steps{
                echo "Performing the scans"
            }
        }
        stage('DeployToDev'){
            steps{
                echo "**** Deploying to Dev Environment ****"
            }
        }
        stage('DeployToTest'){
            steps{
                echo "**** Deploying to Test Environment ****"
            }
        }
        stage('DeployToStage'){
            steps{
                echo "**** Deploying to Stage Environment ****"
            }
        }
        stage('DeployToProd'){
            steps{
                echo "**** Deploying to Prod Environment ****"
            }
        }
    }
}
