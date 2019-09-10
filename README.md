#IsolationForest
構建樹tree的 參數parameters n_estimators是樹的構建數，通常為100即可 n_jobs=2 為使用的核心處理器cpu 如果你填寫-1 那麽就可以 將全部cpu計算資源用來構建樹 max_samples=lendata 最大采樣數，Iforest 不建議過多采樣，封頂建議為256 再多就有可能使樹無法更好采集特征 max_features=5 最大特征數，如果你對特征不是很了解，我說個通俗的，那就是大多數情況有幾列數據或幾行就代表幾個特征或幾個-1個特征。 更細的就是數據集描述這組數據的基本都可以叫做特征。 更多參數方法：<br>
http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.IsolationForest.html#sklearn.ensemble.IsolationForest.predict

Iso_anomaly_score 為異常分數 評分越低，則越是異常 Iso_predict 為粗暴的判斷是否為異常，1是正常，-1是異常 threshold 閾值定義 也可以 根據實際情況手動添加也可以根據不同情況以公式表示，這裏我設置默認為-0.1
