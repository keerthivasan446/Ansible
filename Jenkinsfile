node {
    stage('Git Clone'){
        git credentialsId: 'd4586f90-dc1f-4bc6-a255-58bd271ce364', url: 'https://github.com/keerthivasan446/Ansible.git'
       sh label: '', script: ''' cd /var/tmp/
       rm -rf Ansible
        git clone https://github.com/keerthivasan446/Ansible.git
        cd Ansible
        ls -al'''
    }
    stage('Notification'){
        mail bcc: '', body: "Jenkins job ${env.JOB_NAME} - build ${env.BUILD_NUMBER} ${currentBuild.currentResult}  ${env.JOB_URL} is completed successfully. ", cc: '', from: '', replyTo: '', subject: 'Success Message', to: 'keerthivasan446@gmail.com'
    }
}
