pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file using a shell script
                
                build 'PES2UG21CS462-1'
                sh 'g++ -o obj main/hello.c'
                //sh 'g++ -o obj main/hello.cpp'
            }
        }

        stage('Test') {
            steps {
                // Print the output of the compiled .cpp file
                sh './obj'
            }
        }

        stage('Deploy') {
            steps {
              echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
