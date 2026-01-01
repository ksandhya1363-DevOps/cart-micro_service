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
                //v1.2.3
                tag pattern: "v\\d{1,2}.v\\d{1,2}.v\\d{1,2}", comparator: "REGEXP"
            }
            steps{
                echo "**** Deploying to Prod Environment ****"
            }
        }
    }
}
