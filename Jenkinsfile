pipeline {
    agent any

    stages {

        stage('Python Build') {
            steps {
                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" --version'
                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" HelloWorld.py'
            }
        }

        stage('Maven Version') {
            steps {
                bat 'mvn -version'
            }
        }

        stage('Maven Build') {
            steps {
                bat 'mvn -f MavenHelloWorld/pom.xml clean package'
            }
        }
    }
}