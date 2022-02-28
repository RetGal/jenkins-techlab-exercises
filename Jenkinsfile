pipeline {
    agent {
        // docker build -f Dockerfile -t test-app:latest .
        dockerfile {
            filename 'Dockerfile'
            dir '.'
            args '-t test-app:latest'
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
