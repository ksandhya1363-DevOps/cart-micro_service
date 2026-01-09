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
        name: 'DeployToEnv',
        choices: ['dev','test','stage'],
        description: 'Which env should we deploy'
    )
        choice(
            name: 'TSETING_DONE',
        defaultValue: 'Yes',
        choice:['me','others'],
        description:'We have completed testing'
        )
    booleanParam(
        name: 'TOOGLE',
        defaultValue: true,
        description: 'Is this release approved by SRE??? ',
    )
    text(
        name: 'ReleaseDetails',
        defaultValue: '',
        description: 'Enter some details about what is deploying today'
    )
    }
    stages{
        stage('ParameterStage'){
                steps{
                    echo "Hello, ${params.Person}"
                    echo "Release Notes: ${params.ReleaseDetails}"
                    echo "Is this release approved by SRE??? ${param.TOOGLE}"
                    echo "Selected Env to Deploy is : ${params.DeployToEnv}"
                }
        }
    }
}
