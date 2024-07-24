pipeline {
    agent any

    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'Should we deploy after build?')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building branch ${params.BRANCH_NAME}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            when {
                expression {
                    return params.DEPLOY
                }
            }
            steps {
                echo 'Deploying...'
            }
        }
    }
}

