# cnn_img_discriminater

CNN を使った、簡単な画像判別機のコードです。
3層のconv層を使った、CNNとなっています。
精度は1500回して、だいたい88%、10,000回して84%程度です。
バッチノーマライゼーションとかハイパーパラメータの調整頑張ったらもうちょっと上がるんではないでしょうか？
今回は簡単なアーキテクチャの作成のため、この程度の精度でもよしとしています(笑)

これは　Google の Colab を使うことが前提で書かれているコードです。 Colabじゃないと動かない部分もありますので、ご了承ください。

## Usage
**Image import:**
`uploaded = files.upload()`
上のコードを回して、手動でアップロードしましょう。
npy ファイルは、同じ階層のディレクトリに入っています。
**Training:**
`history = model.fit(X_train, Y_train, batch_size=BATCH_SIZE, epochs=MAX_EPOCH,
                   validation_data = (X_test, Y_test), verbose = 1)`
上記のコードを回しましょう。trainが始まります。
**Predict:**
`model.predict(img_data)`
上記のコードを回しましょう。
カッコ内の img_data に任意の画像リストを入れることで、学習したモデルでの予測ができます。
