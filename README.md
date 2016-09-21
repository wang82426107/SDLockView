# SDLockView
一个基于贝塞尔曲线的手势解锁View

![](http://upload-images.jianshu.io/upload_images/1396375-7c33aa1b9badef51.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




有很多时候,我们需要快速生成SDLockView页面,这时候,对其,我们只需要简简单单的三步,就可以快速集成SDLockView.首先,我们要把Demo中的SDLockView文件夹拖入目标工程中.其中文件夹中包含了SDLockView实现类,UIImage+SizeUpdata(关于修改图片尺寸的延展),和两个图标.

![](http://upload-images.jianshu.io/upload_images/1396375-53ff82bd1e37c6e6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

紧接着就是初始化我们的SDLockView对象,我们要选定它的LockViewType类型,LockViewType为一个枚举类型的数据.

```
typedef enum  {
    SetPassWordType,//设置密码类型界面
    UpdataPassWordType,//修改密码类型界面
    TestingPassWordType,//验证密码类型界面
} LockViewType;


```
选好类型之后,我们直接可以创建SDLockView页面了.
```
SDLockView *view = [SDLockView initWithLockViewType:self.lockViewType];

```
最后添加到我们的视图上即可.
```
[self.view addSubview:view];

```

