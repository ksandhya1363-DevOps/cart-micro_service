pipeline{
    agent{
        label 'java-slave'
    }
    parameters{
        string(
            name: 'Person',
            defaultValue: 'Sandhya',
            description: 'What is your name'
        ) 
    }
    stages{
        stage('ParameterStage'){
                steps{
                    echo "Hello, ${params.Person}"
                }
        }
    }
}
