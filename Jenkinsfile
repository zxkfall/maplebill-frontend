node {
    git url: 'git@github.com:zxkfall/maplebill-frontend.git', branch: 'main'
    stage('Checkout') {
        sh 'echo "Start checkout"'
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'bb1888fd-28ab-4f93-9787-d1171bc39a3d', url: 'git@github.com:zxkfall/maplebill-frontend.git']]])
    }
    stage('Build') {
        sh 'echo "Building"'
        sh 'npm install'
    }
    stage('Deploy') {
        sh 'npm start'
        sh 'echo "Finish"'
    }
}
