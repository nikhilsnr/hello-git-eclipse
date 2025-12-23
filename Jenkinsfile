pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
    }

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code'
                bat 'javac src/com/example/git/HelloGit.java'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running HelloGit class'
                bat 'java -cp src com.example.git.HelloGit'
            }
        }
    }

    post {
        success {
            echo 'Build and execution successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
