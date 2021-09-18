pipeline {
    agent {
        label 'Jenkins-Node'
    }
    environment {
        //be sure to replace "willbla" with your own Docker Hub username
        DOCKER_IMAGE_NAME = "100919861986/train-schedule"
    }
    stages {
        stage('DeployToProduction') {
            when {
                branch 'master'
            }
            steps {
		    script{
			sh("ls")
		    	sh("kubectl apply -f train-schedule-kube.yml")
		    }
            }
        }
    }
}
