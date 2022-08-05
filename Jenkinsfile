pipeline {
    agent any

    environment {
        USER_NAME = "muna"
        USER_ID = 12
    }

    stages {
        stage('List env vars') {
            steps {
                sh "printenv | sort"
            }
        }
        stage('Build number') {
            steps {
                echo "Build_Number = ${env.BUILD_NUMBER}"
                echo "Current user is ${env.USER_NAME}"
                echo "Current user id is ${env.USER_ID}"

            }
        }
        stage('Stage variable') {
            environment {
                USER_NAME = "Ashanta"
                USER_PATH = "/home/apalei"
            }
            steps {
                echo "User name is ${env.USER_NAME}"
                echo "User path is ${env.USER_PATH"
            }
        }
    }
}