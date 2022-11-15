# Longhornの設定

## Install instruction

1. 既存のlonghornをアンインストールする．

```
helm uninstall longhorn -n longhorn-system
```

2. longhornの設定ファイル values.yml を生成する．

```
helm show values longhorn/longhorn > values.yml
```

3. values.yml の中身を書き換える．

書き換える箇所は， <a href="values.yml">values.yml</a>を参照する．

4. helm installでlonghornをインストールする．

```
helm install longhorn longhorn/longhorn --namespace longhorn-system --create-namespace --version 1.3.2 -f values.yml
```

## Reference

- Longhornのカスタマイズするパラメータの資料
  - [Longhorn | Documentation](https://longhorn.io/docs/1.3.1/references/settings/#guaranteed-engine-manager-cpu)
- Longhornのインストール方法(Helm)
  - [Longhorn | Documentation](https://longhorn.io/docs/1.3.2/deploy/install/install-with-helm/)
