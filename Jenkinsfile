pipeline {
    agent any

    stages {
        stage('Dev') {
            steps {
                echo 'Ok'
                cd
                sh 'chmod +x ${env.WORKSPACE}'
                sh './script.sh'
               
                //sh '''javac Hello.java
                //    java HelloWorld'''
               
            }
        }
    }
    post {
        failure {
            mail bcc: '', body: 'Java program failed', cc: '', from: '', replyTo: '', subject: 'Java Program failure', to: 'akashsangle377@gmail.com'   
        }
        success {
            mail bcc: '', body: 'Java program success', cc: '', from: '', replyTo: '', subject: 'Java Program success', to: 'akashsangle377@gmail.com'
            
        }
    }
}
