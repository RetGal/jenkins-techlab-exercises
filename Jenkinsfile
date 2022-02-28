pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            dir 'build'
            args '-t test-app:latest .'
        }
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        timeout(time: 10, unit: 'MINUTES')
        timestamps()  // Timestamper Plugin
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                echo 'noop!'
            }
        }
    }
}
