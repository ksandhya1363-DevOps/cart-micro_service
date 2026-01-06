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
        stages('ParameterStage'){
                steps{
                    echo "Hello, ${params.Person}"
                }
        }
    }
}
