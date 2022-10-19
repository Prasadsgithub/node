pipeline {
    agent { label 'NODE'}
    options {
        timeout(time: 1, unit: 'HOURS')
    }
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('sourcecode') {
            steps {
                git url: 'https://github.com/Prasadsgithub/node.git', 
                branch: 'main'
            }   
        }
    }
    stages {
        stage( 'Build the code ') {
            steps {
                sh 'npm install'
            }  
        }
    }
}