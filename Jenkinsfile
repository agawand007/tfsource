
stages {
  stage('Checkout') {
   steps {
    // Checkout your Ansible playbook repository
    git branch: 'main', url: 'https://github.com/agawand007/tfsource.git'
   }
  }
  stage('Install Ansible') {
   steps {
    // Install Ansible on the Jenkins agent
   sh 'sudo dnf -y install ansible-core'
  }
 }
 stage('Run Ansible Playbook') {
   steps {
   // Run the Ansible playbook
  sh 'ansible-playbook -i inventory playbook.yaml'
  }
 }
}
}
