
pipeline {
    agent any
    tools {
        jdk "JDK17"
        maven "MAVEN3.9"
    }

    environment {
        SNAP_REPO= 'vprofile-snapshot'
        NEXUS_USER= 'admin'
        NEXUS_PASS= 'Kolkata@2'
        RELEASE_REPO= 'vprofile-release'
        CENTRAL_REPO= 'vpro-meven-central'
        NEXUS_GRP_REPO= 'vpro-maven-group'
        NEXUSIP= '172.31.44.200'
        NEXUSPORT= '8081'
        NEXUS_LOGIN= 'nexuslogin'
    }


    stages {
        stage('Build Job')
            steps {
                sh 'maven -s setting.xml -DskipTests install'
            }
    }

}
