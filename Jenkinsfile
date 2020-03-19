pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/balnor2001/fooproject.git'
            }
            }
        stage('newman') {
            steps {

                sh 'newman run Restful Booker.postman_collection.json --environment Restful Booker.postman_environment1.json --reporters junit'

            }

            post {

                always {

                        junit '**/*xml'

                    }
                }
        }
    }
}