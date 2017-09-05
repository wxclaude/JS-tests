### 实现效果：
输入一段内容，选择不同的语言可以进行朗读。还可以选择不同的语速和语调。

### 知识点：
[SpeechSynthesis API](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis)

-   `SpeechSynthesis.getVoices()`：获取所有的语言列表，代表在当前语音对象上所有可用的语言；
-   `SpeechSynthesis.cancel()`：结束，结束当前的语音状态，并将当前语音内容清空；
-   `SpeechSynthesis.pause()`：暂停，暂停当前的语音状态，当不清空语音内容，可以继续播放；
-   `SpeechSynthesis.speak()`：播放，将文字内容加入到播放序列中并开始播放语音；
-   `SpeechSynthesis.resume()`：继续，当语音处于暂停状态的时候，继续播放该语音；
