pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/balnor2001/fooproject.git'
            }
        stage('newman') {

            steps {

                bat 'newman run Restful_Booker_Facit.postman_collection.json --environment Restful_Booker.postman_environment.json --reporters junit'

            }

            post {

                always {

                        junit '**/*xml'

                    }
                }
        }
        }
    }
}