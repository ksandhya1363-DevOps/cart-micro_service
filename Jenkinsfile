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
        choice(
        name: 'Choose'
        choices: ['one','two','three']
        description: 'pick any number below'
    )
    booleanParam(
        name: 'TOOGLE'
        defaultValue: true,
        description: 'Toogle this value'
    )
    text(
        name: 'ReleaseDetails'
        defaultValue: '',
        description: 'Enter spme details about todays deployement '
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
