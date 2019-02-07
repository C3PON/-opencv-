### 基本操作2：视频

*cv2.VideoCapture() cv2.VideoWrite()*

#### 用摄像头捕获视频
创建一个VideoCapture对象
<br>
参数可以是 设备索引号 、 或者视频文件
<br>
设备索引号指定要使用的摄像头，笔记本内置摄像头就是0，1或其他可以选择其他的摄像头。
<br>
然后就能一帧一帧的捕获视频了，最后别忘了停止捕获。
<br>
`import cv2`
<br>
<br>`cap = cv2.VideoCapture(0)`
<br>`while(True):`
<br>`	ret,frame = cap.read()`
<br>`	gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)`
<br>`	cv2.imshow('frame',gray)`
<br>`	if cv2.waitKey(1) & 0xFF == ord('q'):`
<br>`		break`
<br>`cap.release()`
<br>`cv2.destroyAllWindows()`

<br>
<br>
<br>
<br>
<br>

#### 播放视频文件
<br>
cv2.imwrite('messigray.png',img)
<br>

#### 保存视频


