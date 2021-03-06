<!-- https://developers.weixin.qq.com/miniprogram/dev/api/canvas/create-pattern.html -->

canvasContext.createPattern
===========================

> 基础库 1.9.90 开始支持，低版本需做[兼容处理](https://developers.weixin.qq.com/miniprogram/dev/framework/compatibility.html)

### 定义

对指定的图像创建模式的方法，可在指定的方向上重复元图像

### 语法

    canvasContext.createPattern(image, repetition)
    

### 参数

  属性值       |  类型     |  说明                                                   
---------------|-----------|---------------------------------------------------------
  image        |  String   |  重复的图像源，仅支持包内路径和临时路径                 
  repetition   |  String   |指定如何重复图像，有效值有: repeat, repeat-x, repeat-y, no-repeat

### 例子

    const ctx = wx.createCanvasContext('myCanvas')
    const pattern = ctx.createPattern('/path/to/image', 'repeat-x')
    ctx.fillStyle = pattern
    ctx.fillRect(0, 0, 300, 150)
    ctx.draw()
