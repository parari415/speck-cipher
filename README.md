128ビットの鍵サイズと128ビットのブロックサイズを持つSPECK暗号
一部のファイルの末尾にnullバイトが含まれる可能性あり
  
## Files  
 - speck.c:暗号を実装するメインの c プログラム
 - test_vectors.c:サンプルバイナリ入力ファイルを生成するユーティリティ コード
 - key_128.key:キー値の例 (NSA ペーパーのテスト ベクトルから)
 - vect_cipher128.hex:暗号化された 128 ビットのバイナリ テスト ベクトル
 - vect_plain128.hex:平文の 128 ビットのバイナリテストベクトル 

## 手順
```
make
```
```
./testvect
```
暗号化
```
./speck -k key_128.key -e -i vect_plain128.hex -o output.enc
```
復号
```
./speck -k key_128.key -d -i output.enc -o plain_out.hex
```