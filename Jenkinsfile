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
            when {
                branch 'release-*'
            }
            steps{
                echo "**** Deploying to Stage Environment ****"
            }
        }
        stage('DeployToProd'){
            when{
                expression{
                    BRANCH_NAME == ~ /(production | staging) /
                }
            }
            steps{
                echo "**** Deploying to Prod Environment ****"
            }
        }
    }
}
