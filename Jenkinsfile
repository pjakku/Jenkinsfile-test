pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Build Infra Images') {
	        def doInfra = [:]
                echo "setup Postgres, Pgpool and Barman"
            doInfra['my-redis'] = {
		        echo 'building..'
	        }
            doInfra['my-logstash'] = {
                echo 'building..'            
            }
            doInfra['my-barman'] = {
                echo 'building..'
            }
            doInfra['my-postgres'] = {
                echo 'building..'
            }
            doInfra['my-postgres-repmgr'] = {
                echo 'building..'
            }
            doInfra['my-pgpool'] = {
                echo 'building..'
            }
            parallel doInfra
        }
    }
}

