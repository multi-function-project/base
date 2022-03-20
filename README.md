# base

### GitHubの認証情報

settings.xmlの以下のGitHub情報認証情報を設定しておき、
~/.m2配下に配置しておく
~~~
    <server>
        <id>github</id>
        <username>自分のGitHubID</username>
        <password>GitHubアクセストークン:write:packagesだけで可</password>
    </server>
~~~

#### GraalVMのインストール

参考URL
https://graalvm.github.io/native-build-tools/latest/graalvm-setup.html

~~~
# GraalVMのダウンロード
wget  https://github.com/graalvm/graalvm-ce-dev-builds/releases/download/22.1.0-dev-20220127_2024/graalvm-ce-java11-linux-amd64-dev.tar.gz
# 解凍
tar -xzf graalvm-ce-java11-linux-amd64-dev.tar.gz -C "."
~~~

viを起動して、環境変数の設定
~~~
vi .bashrc
~~~

ファイル末尾に追加
~~~
export GRAALVM_HOME="$HOME/graalvm-ce-java11-22.1.0-dev"
export JAVA_HOME="$GRAALVM_HOME"
export PATH="$GRAALVM_HOME/bin:$PATH"
~~~

環境変数の反映
~~~
source .bashrc
~~~

ツールのインストール
~~~
gu install native-image
~~~