
pipeline {
    
    agent {
       node {
            label 'TQ7000L64-582'
        }
    }

    triggers {
        pollSCM '*/5 * * * *'
    }
    stages {
        stage('Building') {
            steps {
                echo 'Building ...'
                sh 'python3 BuildingStage.py'
                echo 'Doing build stuff ...'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing ...'
                sh 'python3 TestingStage.py'
                echo 'Doing test stuff ...'
            }
        }
        stage('Delivering') {
            steps {
                echo 'Delivering ...'
                sh 'python3 DeliveringStage.py'
                echo 'Doing delivery stuff ...'
            }
        }
    }
        
}
