
##UIFrameButton介绍？

* 继承UIButton，重写layoutSubviews，改变UIButton的imageView和titleLabel的的frame。可以任意该改变UIButtonimageView和titleLabel的的起始位置和中间距离。通过枚举，imageVIew和titleLabel分为上下，左右排列布局





##界面样式

```objectivec
typedef NS_ENUM(NSInteger, UIButtonFrameSttyle)
{

LeftImageWithRightTitleFrameStyle=0,

LeftTitleWithRightImageFrameStyle,

TopImageWithbuttomTitleFrameStyle,

TopTitleWithbuttomImageFrameStyle,
};
```
##代码

```objectivec
    UIFrameButton *btn =({

                    UIFrameButton *newBtn=[[UIFrameButton  alloc] initWithFrame:CGRectMake(10, 10, 300, 300)];
                    [newBtn addTarget:self action:@selector(clikBtn:) forControlEvents:UIControlEventTouchUpInside];
                    newBtn.center =self.view.center;
                    [newBtn setTitleColor:[UIColor blackColor] forState:UIControlStateNormal];
                    [newBtn setImage:[UIImage imageNamed:@"play"] forState:UIControlStateNormal];
                    [newBtn setImage:[UIImage imageNamed:@"play"] forState:UIControlStateHighlighted];

                    [newBtn setTitle:@"点击我,我开始移动" forState:UIControlStateNormal];
                    newBtn.frameStyle =LeftImageWithRightTitleFrameStyle;
                    newBtn.beginDistance =1;
                    newBtn.layer.borderColor = [UIColor grayColor].CGColor;
                    newBtn.layer.cornerRadius = 5;
                    newBtn.layer.borderWidth =1;
                    newBtn.layer.masksToBounds =YES;
                    newBtn;
                    });   
    btn.frameStyle =TopImageWithbuttomTitleFrameStyle; //设置布局样式
    btn.centerDistance =5；//设置image和title的距离
    btn.beginDistance = 5 //设置subViews的开始的距离


```

##有问题反馈
在使用中有任何问题，欢迎反馈给我，可以用以下联系方式跟我交流

* QQ 476804765
* Email:13281250969@163.com

##下一步功能

* 发布到cocoapods
