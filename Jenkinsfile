
pipeline {
    
    agent {
       node {
            label 'TQ7000L64-582'
        }
    }
    
    stages {
        
        stage('Building') {
            steps {
                echo 'Building ...'
                python3 BuildingStage.py
                echo 'Doing build stuff ...'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing ...'
                python3 TestingStage.py
                echo 'Doing test stuff ...'
            }
        }
        stage('Delivering') {
            steps {
                echo 'Delivering ...'
                python3 DeliveringStage.py
                echo 'Doing delivery stuff ...'
            }
        }
    }
        
}
