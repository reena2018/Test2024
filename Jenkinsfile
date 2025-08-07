pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                // Cloning handled by Jenkins SCM config, so this can be empty or skipped
                echo 'Cloning repo...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building C program...'
                // Compile your C file (replace 'program.c' with your filename)
                sh 'gcc -o myprogram Hello.c'
            }
        }

        stage('Test') {
            steps {
                echo 'Running the program as a test...'
                sh './myprogram'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (simulated)'
                // For demo, just copy executable somewhere or echo success
                sh 'cp myprogram /tmp/'
                echo 'Program deployed to /tmp/'
            }
        }
    }
}
