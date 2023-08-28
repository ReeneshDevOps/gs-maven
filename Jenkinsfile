pipeline {
	agent any

	// triggers {
	// 	pollSCM 'H/10 * * * *'
	// }

	// options {
	// 	disableConcurrentBuilds()
	// 	buildDiscarder(logRotator(numToKeepStr: '14'))
	// }

	stages {

                stage("Build"){

                 steps {
                   sh 'mvn clean install -f complete/pom.xml'

                   }
                  }
		stage("test: baseline (jdk8)") {

			steps {
				sh 'test/run.sh'
			}
		}

	}

	
		}
	}
}
