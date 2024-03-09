FROM golang:1.20.5

ENTRYPOINT ["go"]
CMD ["version"]
# go versionが実行される。
# ENTRYPOINTが指定されている場合CMDはその続きのargsになる
# CMDは実行時上書きすることができる。つまり空でrunした時のdefaultの挙動を定義できる。
# ENTRYPOINTを使うことで、今回だとgoコマンドに制限することができる

# シェル形式とexec形式
# ENTRYPOINT ["a", "b"]だと$ a b になり
# ENTRYPOINT a bだと、$ /bin/bash -c a b と解釈される
# なのでシェル形式じゃないと環境変数は展開されない。
# ENTRYPOINT ["/bin/bash", "-c", "echo $HOME"]としたら展開できる
# 参考: https://tech.enechange.co.jp/entry/2022/10/25/100000
