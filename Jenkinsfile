pipeline {
    agent { label 'PLATFORM-ROBOT-DVS-TB-04-Slave-Develop'}
    
    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
    }
}