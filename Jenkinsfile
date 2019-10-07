node("linux"){  
//yo
    timestamps{
    checkout(
        [
            $class: 'GitSCM', 
            branches: [[name: '${sha1}']], 
            doGenerateSubmoduleConfigurations: false, 
            extensions: [
                [$class: 'CleanBeforeCheckout'],
                [$class: 'CloneOption', depth: 0, noTags: true, reference: '', shallow: true]
                ], 
            submoduleCfg: [], 
            userRemoteConfigs: [[
                credentialsId: 'jonathangithub', 
                refspec: '+refs/pull/${ghprbPullId}/*:refs/remotes/origin/pr/${ghprbPullId}/*', 
                url: 'https://github.com/jonathangoorin/somecode.git']]
        ])
        
        sh "touch txt.txt"
    }
}


//some more commits 
//jonathangooringithub