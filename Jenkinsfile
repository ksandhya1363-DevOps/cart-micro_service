pipeline{
    agent{
        label 'java-slave'
    }
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage("DeploytoDev"){
                steps{
                    echo "Deploying to Dev Environment"
                }
            }
        stage('ProdEnv'){
            when{
                anyOf{
                    branch 'production'
                    environment name : 'DEPLOY_TO', value : 'development'
                } 
            }
            steps{
                echo "**** Deploying to Production ****"
            }
        }
    }
}
