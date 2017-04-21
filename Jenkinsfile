node {
    stage 'メッセージを表示'
    sh 'echo Hello World'
    
    stage '日付を表示'
    sh 'date'
    
    stage 'test job実行'
    build 'test job'
    
    stage('test job2実行') {
     try {
         build 'test job2'
     } catch(Exception e) {
        sh 'echo 失敗しました。'
        stage('しっぱいぱい') {
            sh 'git clone https://github.com/bundler/bundler.git'
            echo 'とりあえずbundlerインストールしたよ'
        }
     } finally {
        sh 'echo 処理を終了させます。'
     }
    }
}
