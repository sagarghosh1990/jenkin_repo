pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Users\\MONY SAGAR GHOSH\\AppData\\Local\\Programs\\Python\\Python314\\python.exe'
    }

    stages {
        stage("checkout code") {
            steps {
                checkout scm
            }
            
        }

        stage('debug') {
            steps {
                bat 'whoami'
                bat 'where python'
                bat 'dir "C:\\Users\\MONY SAGAR GHOSH\\AppData\\Local\\Programs\\Python\\Python314"'
            }
        }
        stage('show python version') {
            steps {
                bat "\"${env.PYTHON}\" --version"
            }
        }
        stage('run extract_data.py') {
            steps {
                bat "\"${env.PYTHON}\" extract_data.py"
            }
        }
    }
}