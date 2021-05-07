pipeline {
    agent any

    stages {
        stage('CloneAppGithub') {
            steps {
                git branch: 'main', credentialsId: 'MyGithub', url: 'https://github.com/BorisRadenkovic/Docker_JS_appp.git'

                echo 'Repo cloned!'
            }
        }
        stage('GetDockerCompose') {
            steps {
                sh "sudo cp /home/boris2/boris2_jenkins_home/workspace/Docker_app/docker-compose.yaml /home/boris2"

            }
        }

        stage('CopyToRemote') {
             steps {
                sh "sudo scp /home/boris2/docker-compose.yaml boris3@10.113.80.109:/home/boris3/dockerApp"
            }
        }
       // stage('') {
            // steps {
            //    sh "sudo scp /home/boris2/docker-compose.yaml boris3@10.113.80.1092:/home/boris3/dockerApp"
           //  }
      //  }




    }
}
