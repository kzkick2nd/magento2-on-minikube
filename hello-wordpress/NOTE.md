基本プロセス
1. Dockerfile は既存のもの
2. 永続化ディスクを使う
3. 環境変数から情報を渡す

Add a Secret generator
    kustomization.yaml に secrets を追加する

Add resource configs for MySQL and WordPress
    deployements を2つ追加
    kustomization.yaml に resources を追加

Apply and Verify
    $ kubectl apply -k ./
    $ kubectl get secrets
    $ kubectl get pvc
    $ kubectl get pods
    $ kubectl get services wordpress
    $ minikube service wordpress --url
    $ kubectl delete -k ./
