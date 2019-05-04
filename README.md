# blog_Test3
ブログテスト用リポ

## 別のブログを建てる場合

### Github Pagesの設定
* githubでリポジトリを新たに作成
* とりあえず、READMEを作っておく
* gh-pages という名のブランチを作る

### 記事を置く場所（PC側の設定）
* ディレクトリの移動
* `hexo init [blogname]`
* blogname に移動
* `npm install`
* これで、ブログの骨組みが出来る
* `hexo server` で確認できます
* Hexoの git デプロイプラグインをインストールした 
* `npm install hexo-deployer-git --save`

### _config.yml の修正
* 以下のURL、ROOTを変更し、以下のようにする
* url: https://【ユーザーネーム】.github.io/【リポジトリ名】/
* root: 【リポジトリ名】
```
# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: 'https://pokabu55.github.io/blog_Test3/'
root: 'blog_Test3'
permalink: :year/:month/:day/:title/
permalink_defaults:
```
* もう1個、変更
type, repo, branch を以下のように変更。
```
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: 'https://github.com/pokabu55/blog_Test3.git'
  branch: gh-pages
```
### デプロイ
* `hexo deploy` で、OK。

以上。
