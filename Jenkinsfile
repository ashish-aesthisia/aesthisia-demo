pipeline {
    agent any
    parameters {
        string(name: "ver1", defaultValue: "vans", trim: true, description: "tag parameter")
    }
    stages {
        stage("Build") {
            steps {
                echo "Build stage."
                echo "Hello $params.ver1"
                sh 'docker build dockerfile.dev -t  $params.ver1'
                sh 'docker run -p 3000:3000'
            }
        }
        stage("Test") {
            steps {
                echo "Test stage."
            }
        }
        stage("Release") {
            steps {
                echo "Release stage."
            }
        }
    }
}
