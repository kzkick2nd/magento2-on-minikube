基本プロセス
- Dockerfileは既存のものを使う bitnami/magento OK
- pvc OK
- secrets を kustomization から渡す OK
- 環境変数から情報を渡す OK

https://github.com/bitnami/bitnami-docker-magento
リンク切れ発見

備考
bitnami/magento の ip が決め撃ちなので起動不能だった
考えてみれば、helm の magento も一回起動してから設定を更新する無理筋な方法をとっていた
magento 初回起動時の ip についてどうすればよいか考える必要がある