pipeline{
    agent {
        lable 'java-slave'
    }
    stages{
        stage('Build'){
            steps{
                echo "***** Building the application *****"
            }
        }
    }
    post{
        //this will only run, when the current pipeline or stae is having the success stage
        success{
            echo "**** Post ===========>>> Success is triggered ****"
            //mail logic
        }
        //Runs only when stage or pipeline is having the failure stage
        failure{
            echo "***** Post =========>>> Failure is triggered"
            //mail logic
        }
        //Runs even the pipeline or stage failed or success, irrespective of them it should run everytime
        always{
            //mail logic
            echo "***** Post ==========>>> Pipeline executed *****"
        }
    }
}
