train.csvを参考にtest.csvのSurvivedの値を予測するコンペティションです。
データ前処理: train.csv、test.csv、gender_submission.csv データセットを確認します。データを調べて構造を理解し、必要に応じてクリーンアップします。

（予測手順）
モデルのトレーニング: train.csv データセットを使用して、利用可能な機能に基づいて Survived 列を予測する機械学習モデルをトレーニングします。

予測: モデルのトレーニングが完了したら、それを使用して test.csv の乗客の Survived 列を予測します。

CSV 出力: gender_submission.csv で提供される形式で予測を含む CSV ファイルを生成します。

トレーニング データ (train.csv): PassengerId、Survived、Pclass、Name、Sex、Age、SibSp、Parch、Ticket、Fare、Cabin、Embarked の列が含まれます。ターゲット変数は Survived です。

テスト データ (test.csv): トレーニング データに似ていますが、Survived 列がありません。

性別の提出 (gender_submission.csv): PassengerId と Survived が含まれており、提出形式の参照として機能します。

（予測作業）
データの前処理: 欠損値を処理し、カテゴリ変数をエンコードします。
モデルのトレーニング: train.csv データで機械学習モデルをトレーニングします。
予測: トレーニングされたモデルを使用して、test.csv の乗客の生存を予測します。
ここで前処理に進みます。

RandomForest モデルでトレーニングしてモデルを構築します。検証セットで 82.12% の精度を達成しました。
test.csv データの最初の５個の予測を試行しました。予測は次のとおりです。

乗客 892: 生存 = 0
乗客 893: 生存 = 0
乗客 894: 生存 = 0
乗客 895: 生存 = 1
乗客 896: 生存 = 0

次に、test.csv ファイル内のすべての乗客の最終的な予測を生成し、gender_submission.csv を参考にした CSV 形式で結果をエクスポートします。

このファイルには、test.csv データセット内の各乗客の PassengerId と予測された生存値が含まれています。

上記手法にて生成した　submission.csv　のスコアは　0.74641　でした。
