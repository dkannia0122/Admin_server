Pipeleine {
 node (label: 'viis'){
  stage("ssh-agent") {
    sshagent (credentials : ['admin_server']) {
    stage ('Fill_CM_Vars.xml') {
      sh 'commissioningManager.sh file=/opt/commissioning/workflow/xmls/install/Fill_CM_Vars.xml content'
      input("Ready to proceed?")
      }
    stage ('Initialize_Admin_server') {
        sh 'commissioningManager.sh file=/opt/commissioning/workflow/xmls/install/Initialize_Admin_Server.xml content'
        input("Ready to Proceed?")
    }
    }
  }
}
}
