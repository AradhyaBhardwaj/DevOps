
pipeline {
    agent any

    environment {
        JAVA_HOME = 'C:\\Program Files\\Java\\jdk-21.0.12.1'
    }

    stages {

        stage('Python Build') {
            steps {
                echo 'Checking Python Installation'

                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" --version'

                echo 'Running Python Program'

                bat '"C:\\Users\\aradh\\AppData\\Local\\Python\\bin\\python.exe" HelloWorld.py'
            }
        }

        stage('Maven Version') {
            steps {
                echo 'Checking Maven Installation'

                bat '"C:\\Program Files\\apache-maven-3.10.0\\bin\\mvn.cmd" -version'
            }
        }

        stage('Maven Build') {
            steps {
                echo 'Building Java Maven Project'

                bat '"C:\\Program Files\\apache-maven-3.10.0\\bin\\mvn.cmd" -f "Maven Java\\pom.xml" clean package'
            }
        }

        stage('Run JAR') {
            steps {
                echo 'Executing Generated JAR'

                bat '"%JAVA_HOME%\\bin\\java.exe" -jar "Maven Java\\target\\maven-hello-world-1.0.jar"'
            }
        }
    }

    post {
        success {
            echo 'ALL STAGES COMPLETED SUCCESSFULLY!'
        }

        failure {
            echo 'PIPELINE FAILED - CHECK CONSOLE OUTPUT'
        }
    }
}
