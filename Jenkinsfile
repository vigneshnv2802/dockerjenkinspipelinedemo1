node {

	stage('Clone repository') {

		checkout scm

	}

	stage('Build image') {

		app = docker.build("dockerjenkinspipelineproj")

	}

	stage('Deploy') {

		sh ("docker run -d -p 8087:80 dockerjenkinspipelineproj")

	}

	stage('Remove old images') {

		sh("docker rmi dockerjenkinspipelineproj:latest -f")

   }

}


