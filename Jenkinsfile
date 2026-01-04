pipeline{
    agent{
        lable 'java-slave'
    }
    stages{
        stage('Build'){
            steps{
                 echo "Building the application"
            }
        }
        stage('ParallelStageScans'){
            parallel{
                stage('Sonar'){
                    steps{
                        echo "Sonar scan is executing"
                        sleep(10)
                    }
                }
                stage('Fortify'){
                    steps{
                        echo "Fortify scan is executing"
                        sleep(10)
                    }
                }
                stage('Prisma'){
                    steps{
                        echo "Prisma scan is executing"
                        sleep(10)
                    }
                }
            }
        }
    }
}
