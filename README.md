# react-simple-app

- このプロジェクトで色々試したいからmonorepoが良さそうだけど、設定だるいしハマりたくない
- とりあえず試すだけなのでルートプロジェクト配下にどかどか置くでいい
- vscodeもプロジェクトごとに別窓で立ち上げる

## ■試したこと

### ●create-react-app

```sh
npx create-react-app projects/just-login --template typescript
cp -f .gitignore projects/just-login/.gitignore
code projects/just-login
```

### ●VSCodeでデバッグ実行したい

- 試した場所
  - projects/just-login
- [Visual Studio CodeでできるReactアプリの便利なデバッグ方法](https://fintan.jp/page/462/)でできた
  - launch.jsonの`configurations/type`を`pwa-chrome`から`chrome`に変更

### ●未ログインだったらリダイレクトしたい

pages/Login - Amazon Cognito -> pages/Home

```txt
🤓 --> Login --> Amazon Cognito

✅ OK --> Home
🔥 NG --> Login
```

```txt
🤓 --> Home

✅ Logged in.     --> Home
🔥 Not logged in. --> Home
```
