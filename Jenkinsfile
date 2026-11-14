
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
                bat '"C:\\Program Files\\apache-maven-3.10.0\\bin\\mvn.cmd" -version'
            }
        }

        stage('Maven Build') {
            steps {
                bat '"C:\\Program Files\\apache-maven-3.10.0\\bin\\mvn.cmd" -f MavenHelloWorld\\pom.xml clean package'
            }
        }

        stage('Run JAR') {
            steps {
                bat 'java -jar MavenHelloWorld\\target\\maven-hello-world-1.0.jar'
            }
        }
    }
}
