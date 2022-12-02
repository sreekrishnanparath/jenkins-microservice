
// scripted
//node {
//    echo "Build"
//    echo "Test"
//    echo "Integration Test"
//}

// Declarative
pipeline {
    //agent any
    agent { docker { image 'maven' } }
	stages  {
	    stage('Build') {
	        steps {
	            sh "mvn --version"
	        }
	    }
	    stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
	}
	post {
	    always {
	        echo "Iam awesome. I run always"
	    }
	    success {
            echo "I run when you are successful"
        }
        failure {
            echo "I run when you fail"
        }
	}
}
