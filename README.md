# Git Lesson

## リモートリポジトリとローカルリポジトリとはそれぞれ何でしょうか？
* リモートリポジトリはネット上にある共有のソースコードの管理場所
* ローカルリポジトリは個々のPC内にあるソースコードの管理場所


## プッシュとマージの違いは何でしょうか？
* プッシュはローカルで変更した内容をリモートリポジトリに反映させる。
* マージは各ブランチの変更した内容をブランチに反映させる。


## コミットとプッシュの違い
* コミットはローカルリポジトリで行った変更内容をローカルリポジトリ内で保存を行う
* プッシュはローカルリポジトリで行った変更内容をリモートリポジトリに保存を行う


## コミットのメッセージはどのように書いてあげるのが最適でしょうか？
* どんな変更内容をしたか一目でわかるように書く
 * 例として、検索ボタンのソースコードを変えた場合、コミットメッセージを検索ボタン変更にするなど
 * 今回のプルリクを作成するために残したコミットメッセージは一部のことになっている為、適切ではないと考えます。
* プレフィックスとは、どのような変更を何のために追加したかわかりやすいように表記する
 * 例：ftat: ネットワーク通信するため、hogeを追加
 * frat:新しい機能　fix:バグの修正　docs:ドキュメントの変更　style:空白　test:テスト関連



## ローカルでマージするフローと、プルリクエストでマージするフローの違いは何でしょうか？
- ローカルでマージするフロー
 - ローカルは自分で作成したブランチでソースコードを変更しマージで各ブランチの内容を反映する、リモートのマスターに自分でプッシュする。
 - メリット:自分の保管場所のみ変更保存されるので、同時進行で作業を行える。
 - デメリット:コードレビューを挟まないので、バグがあっても気づかないで本番環境にアップされる可能性がある


- プルリクエストでマージするフロー
 - プルリクエストをしたいファイルを追記などした後、リモートの作業中のブランチに反映させ、プッシュ確認をしたら、ブラウザでリモートリポジトリを確認し、プルリクエストを作成する
  - メリット：本番環境に反映する前に管理者権限のある者が確認するので、事前にバグを発見する事ができる。
  - デメリット：リモート上でマージした内容を、ローカルのマスターには反映されない



## コンフリクトを起こしてしまった場合、どう対処すべきですか？
1. 先にマージされた変更内容を取り込む
2. 後にマージしようとしている変更内容を取り込む
3. どちらの変更内容も取り込む