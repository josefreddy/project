node ('sub'){
    stage('c Download'){
        git 'https://github.com/intelliqittrainings/maven.git'
    }
    stage('c Building'){
        sh label: '', script: 'mvn package'
    }
    stage('c Deploying'){
        sh label: '', script: 'scp /home/ubuntu/workspace/workspace/"scripted pipe"/webapp/target/webapp.war ubuntu@10.0.1.89:/var/lib/tomcat9/webapps/testing1.war'
    }
    stage('c Tes'){
        git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
        sh label: '', script: 'java -jar testing.jar'
    }
    stage('c delivary'){
        
        sh label: '', script: 'echo "success of automation"'
       
    }
    stage('c ddelivery of subbu'){
        sshagent(['ssh-tomct']) {
    sh 'scp -o StrictHostKeyChecking=no /home/ubuntu/workspace/workspace/"scripted pipe"/webapp/target/webapp.war ubuntu@10.0.1.16:/var/lib/tomcat9/webapps/subbu'
}
}
}   
    
