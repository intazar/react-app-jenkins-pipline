pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                echo "Build Part Starts Here" 
                sh "sudo npm install"
                sh "sudo npm run build"
                echo "Build Part Ends Here" 
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /var/www/react-app"
                sh "sudo cp -r ${WORKSPACE}/build/ /var/www/react-app/"
            }
        }
    }
}
