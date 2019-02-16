### 图像的读取、显示、保存
cv2.imread() cv2.imshow() cv2.imwrite()

`import cv2`
<br>
`img = cv2.imread('messi5.jpg',0)`

cv2.imread()用于读入图像，这幅图想应该在程序的工作路径下或提供完整路径，第二个参数是要告诉函数该如何读取这幅图片。• cv2.IMREAD_COLOR 默认 彩色 忽略透明度
<br>
cv2.IMREAD_GRAYSCALE以灰度模式读入图像
<br>
cv2.IMREAD_UNCHANGED 读入一幅图像虽并且包括图像的 alpha 通道
<br>
路径错误时不会报错
<br>
<br>
`cv2.imshow('image',img)`
<br>
`cv2.waitKey(0)`
<br>
`cv2.destroyAllWindows()`
<br>
`cv2.imshow()`
<br>
窗口自动调整为图像大小
<br>
cv2.imshow()第一个参数是窗口名字，第二个是图像
<br>
cv2.waitKey()键盘绑定函数，时间尺度是毫秒级，0为无限等待
<br>
cv2.imshow()删除任何窗口 删除特定窗口 cv2.destroyWindow()
<br>
保存图像
<br>
cv2.imwrite('messigray.png',img)
<br>

#### 练习 加载一个灰度图，显示图片，按下’s’保存退出，按下esc不保存退出

`import numpy as np`
<br>
`import cv2 `
<br>
<br>
`img = cv2.imread('messi5.jpg',0) `
<br>
`cv2.imshow('image',img)`<br>
`k = cv2.waitKey(0) `<br>
`if k == 27: # wait for ESC key to exit `<br>
`    cv2.destroyAllWindows() `<br>
`elif k == ord('s'): # wait for 's' key to save and exit `<br>
`	cv2.imwrite('messigray.png',img) `<br>
`	cv2.destroyAllWindows()`<br>
