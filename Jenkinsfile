pipeline{
    agent{
        label 'java-slave'
    }
    environment{
        DEPLOY_TO = 'development'
    }
    stages{
        stage("DeploytoDev"){
                steps{
                    echo "Deploying to Dev Environment"
                }
            }
        stage('ProdEnv'){
            when{
                allOf{
                    branch 'production'
                    environment name : 'DEPLOY_TO', value : 'production'
                } 
            }
            steps{
                echo "**** Deploying to Production ****"
            }
        }
    }
}
