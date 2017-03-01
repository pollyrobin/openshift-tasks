node('jdk8') {
    def mvnHome = tool 'M3'
    def mvnCmd = "${mvnHome}/bin/mvn -s ${env.JENKINS_HOME}/settings.xml"
    def ocCmd = "/usr/bin/oc --token=`cat /var/run/secrets/kubernetes.io/serviceaccount/token` --server=https://openshift.default.svc.cluster.local --certificate-authority=/run/secrets/kubernetes.io/serviceaccount/ca.crt"

    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
