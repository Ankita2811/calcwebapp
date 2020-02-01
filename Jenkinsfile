node{
    stage('Git pipeline Clone'){
        git 'https://github.com/Ankita2811/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
