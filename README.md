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