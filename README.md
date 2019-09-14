# Kubernetes from zero  to Hero  
このリポジトリはKubernetesの初心者や経験の少ない人がレベルアップするためのハンズオン資料です。実行環境を作成していち早くアプリケーションを動作させたい場合は『Kubernetesクラスターにアプリケーションをデプロイする』に進んでください。一つ一つのコンポーネントの役割を学びながらアプリケーションをデプロイしたい人は『Kubernetesクラスターにアプリケーションをデプロイする』と『各コンポーネントの説明』を交互に参照しながら進めてください。  

## 目次  
- 実行環境  
- Kubernetesの概要
- Kubernetesクラスターにアプリケーションをデプロイする  
- 各コンポーネントの説明
## 実行環境  
- docker desktop  2.1.0.2
- kubectl  1.14.6  

## Kubernetesの概要  

## Kubernetesクラスターにアプリケーションをデプロイする   

```
$ git clone https://github.com/takapon564/KubernetesFromZeroToHero.git  

$ cd KubernetesFromZeroToHero  

# データベースのデプロイ
$ kubectl apply -f manifest/database/

# 環境変数のConfigMapを展開
kubectl apply -f manifest/configuration/

# データベースのマイグレーション
$ kubectl apply -f manifest/migrate/

# アプリケーションのdeploy
$ kubectl apply -f manifest/application/

# ingressコントローラーの有効化
$ matsuuratakahito$ ./ingress-controller-setup.sh

# アプリケーションを外部に公開するためのservice設定
$ kubectl apply -f manifest/service/
```  

ブラウザで`localost`にアクセス  
![](./images/app.jpg)  


## 各コンポーネントの説明  
### Deployment, Persistence  Volume  

### ConfigMap  

### job  

### Service, Ingress
