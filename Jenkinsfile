pipeline {

    agent any

    environment {

        LANG = 'en_US.UTF-8'
        LC_ALL = 'en_US.UTF-8'

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
    }
}
