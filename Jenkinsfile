pipeline {
    agent any
    stages {
        stage('clean repo') {
            steps {
                bat "rmdir /s /q myjenkindemo"
                bat "git clone https://github.com/abhib5/myjenkindemo.git"
                bat "mvn clean -f myjenkindemo"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f myjenkindemo"
                
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f myjenkindemo"
                
            }
        }
    }
}