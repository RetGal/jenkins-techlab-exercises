pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'Greetings_to', defaultValue: 'Jenkins Techlab', description: 'Who to greet?')
        string(name: 'Greetings_from', defaultValue: 'Reto', description: 'Who greets?')
    }
    stages {
        stage('Greeting') {
            steps {
                echo "${params.Greetings_from}: Hello, ${params.Greetings_to}!"
            }
        }
    }
}
