pipeline {

    agent any

    environment {

        LANG = 'en_US.UTF-8'
        LC_ALL = 'en_US.UTF-8'

    }

    tools {

        gradle 'Gradle'

    }

    stages {

        stage('Checkout') {

            steps {

                git branch: 'master',
                url: 'https://github.com/harshithxr/ext-4.git'

            }
        }

        stage('Build') {

            steps {

                sh 'gradle build -x test'

            }
        }

        stage('Run') {

            steps {

                sh 'java -jar build/libs/MyMavenToGradle-1.0-SNAPSHOT.jar'

            }
        }
    }
}
