pipeline {
    agent { label 'PLATFORM-ROBOT-DVS-TB-04-Slave-Develop' }

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker images -a'
                sh '''cd azure-vote/
                    docker images -a
                    docker build -t jenkins-pipeline .
                    docker images -a
                    cd ..'''
            }
        }
    }
}
