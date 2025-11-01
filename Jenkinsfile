node {
    stage('Checkout') {
        git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic.git'
    }

    stage('Build') {
        env.JAVA_HOME = '/opt/homebrew/opt/openjdk@25'
        env.PATH = "${env.JAVA_HOME}/bin:/Users/heril/.jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven-3.9.9/bin:${env.PATH}"
        sh 'mvn clean package'
    }

    stage('Test') {
        env.JAVA_HOME = '/opt/homebrew/opt/openjdk@25'
        env.PATH = "${env.JAVA_HOME}/bin:/Users/heril/.jenkins/tools/hudson.tasks.Maven_MavenInstallation/Maven-3.9.9/bin:${env.PATH}"
        sh 'mvn test'
    }
}

