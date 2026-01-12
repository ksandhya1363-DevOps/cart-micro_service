pipeline{
    agent{
        label 'java-slave'
    }
    stages{
        stage('Build'){
            steps{
                echo "****Building maven application****"
            }
        }
        stage('CodeAnalysis'){
            steps{
                echo "Running the sonar scan"
            }
        }
        stage('DockerBuildnPush'){
            steps{
                echo "Build and Push Docker images"
            }
        }
        stage('DeployToDev'){
            steps{
                echo "**** Deploing to Dev Environment ****"
            }
        }
        stage('DeployToTest'){
            steps{
                echo "**** Deploying to Test Env ****"
            }
        }
        stage('DeployToProd'){
            options{
               timeout (time: 120, unit: 'SECONDS')
            }
            input{
                message "Doing Prod Deployment?????"
                ok 'yes'
                submitter 'ksandhyajenkins,sandhyadev'
            }
            steps{
                echo "**** Deploying to Prod Env ****"
            }
        }

    }
}
