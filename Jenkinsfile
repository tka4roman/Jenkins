pipeline {
    agent any
    stages {
        stage('Hello World!') {
            steps {
                sh 'cd /home/rtk/Documents/JenkinsProj/Jenkins'
                sh 'git pull'
                sh './hello.py'
                sh 'echo "Your commit is: $(git log -1 --pretty=tformat:%h)"'
            }
        }
    }
}

