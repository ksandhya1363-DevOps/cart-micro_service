pipeline{
    //agent any
  agent{
        label 'java-slave2'
    }
    stages {
            stage('Build'){
                steps{
                    echo "This is a build stage"
                    sleep 20
                    echo "Sleep is completed"
                }
            }
            stage('groovycodestage'){
                steps{
                    script{
                        def course = "k8s"
                        if (course == "k8s")
                        println("Thanks for enrolling to k8s course")
                        else
                        println("Do enrollment to k8s")
                    }
                }
            }
    }
}
