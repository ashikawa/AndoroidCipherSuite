# 話の発端

<http://www.jnsa.org/seminar/pki-day/2011/data/03_mutoh.pdf>

# 外部からの接続確認

    openssl s_client -connect [HOST]:443 -cipher [CIPHER SUITE]

# 迷ったら

    man ciphers

# Apache 設定の確認方法

    openssl ciphers -v 'ALL:!ADH:!EXPORT:!SSLv2:+HIGH:+MEDIUM:!LOW:!DES:!RC4:!MD5' | sort

    AES128-SHA              SSLv3 Kx=RSA      Au=RSA  Enc=AES(128)  Mac=SHA1
    AES256-SHA              SSLv3 Kx=RSA      Au=RSA  Enc=AES(256)  Mac=SHA1
    CAMELLIA128-SHA         SSLv3 Kx=RSA      Au=RSA  Enc=Camellia(128) Mac=SHA1
    CAMELLIA256-SHA         SSLv3 Kx=RSA      Au=RSA  Enc=Camellia(256) Mac=SHA1
    DES-CBC3-SHA            SSLv3 Kx=RSA      Au=RSA  Enc=3DES(168) Mac=SHA1
    (略)

# 推奨設定(仮)

    ALL:!ADH:!EXPORT:!SSLv2:+HIGH:+MEDIUM:!LOW:!DES:!RC4:!MD5

※ Softbank と AU で調査機種が足りないと思われる。
