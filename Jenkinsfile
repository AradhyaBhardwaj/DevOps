pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" --version'
            }
        }

        stage('Run Hello World') {
            steps {
                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" HelloWorld.py'
            }
        }
    }
}