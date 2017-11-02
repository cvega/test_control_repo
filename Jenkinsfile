    node {
        stage(item) {
            git checkout
            sh """sed -i -e "/mod \'${puppet_module}\'/{n;n;s/.*/  :tag => \'${tag}\'/}" PuppetFile"""
        }
    }
    timeout(time: 5, unit: 'MINUTES') {
        input 'deploy?'
    }
