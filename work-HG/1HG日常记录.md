#
[链接文本](https://www.github.com)
软件发开流程 、设计模式、体系结构
# 黑谷账号类型
- 客户
  - 18030251225
- 销售
  - 18030251224
- 内部账号
  - 18030251223
- 体验账号
# 人才猎手 多选地址
【增加多选地址功能】
https://www.tapd.cn/37438467/prong/stories/view/1137438467001008398

新增字段
TTJobListModel -》mulAddr
HGJobModel： -》
NSArray <JobCompWorkAddressModel *> *workAddressList;// 工作地址
JobCompWorkAddressModel -》 BOOL isSelectedLocal; 本地选中

/heygood-recruit/company/common/getCompJobCateList
接口增加返回 mulAddr 字段 0：表示不支持多地址，1：表示支持多地址

/post/recruitPost/add
/post/recruitPost/edit
这两个接口中，workAddressId 存多个地址id用逗号(,)分隔

/post/recruitPost/list
/post/recruitPost/queryById
这两个接口返回的对象，原来的 workAddress改成了 workAddressList。

# 4.28
```objc
- (UITableViewCell *)tableView:(UITableView *)tableView cellForRowAtIndexPath:(NSIndexPath *)indexPath {
    HGAddWxChooseTableCell *cell = [tableView dequeueReusableCellWithIdentifier:@"HGAddWxChooseTableCell" forIndexPath:indexPath];

    // 配置 cell 的代码

    if (self.isMultiSelect) {
        // 多选模式
        cell.checkBoxBlock = ^(BOOL selected) {
            if (selected) {
                // 如果未选中，则添加该行的索引
                [self.selectedRows addObject:indexPath];
            } else {
                // 如果已选中，则移除该行的索引
                [self.selectedRows removeObject:indexPath];
            }
        };
    } else {
        // 单选模式
        cell.checkBoxBlock = ^(BOOL selected) {
            if (selected) {
                // 如果选中，则将当前行的索引设置为选中行
                self.selectedRow = indexPath;
            } else {
                // 如果取消选中，则将选中行设置为无效值
                self.selectedRow = nil;
            }
        };

        // 根据当前行是否为选中行来设置选中状态
        cell.checkBoxSelected = [indexPath isEqual:self.selectedRow];
    }

    return cell;
}
```
// 颜色
UIImage *colorImg = [UIImage gradientColorImageFromColors:@[JHColorHex(0x7F5AFF),JHColorHex(0x1BD0FF)] gradientType:GradientTypeLeftToRight imgSize:CGSizeMake(50, 50)];
[button setBackgroundImage:colorImg forState:UIControlStateNormal];

# 4.27
HGCustomerPrivateLetterView
HGCustomerPrivateLetterView *letterView = [[NSBundle mainBundle] loadNibNamed:@"HGCustomerPrivateLetterView" owner:nil options:nil][0];
  letterView.type = 4;
  letterView.privateLetter = @"";
  letterView.businessId = @"";
  [letterView showMenu:YES];


HGMsgAccountTableViewCell

//训练抖音超级销售 基础信息
            HGAccountListViewController *vc = [[HGAccountListViewController alloc] init];
            vc.viewType = 1;
            vc.isFromDouyinHuoke = YES;
            [self.navigationController pushViewController:vc animated:YES];


# 4.26

// url  HGAppCatchCst
http://wgz:wgz2024%@8.136.240.199:10101/r/HGAppCatchCst.git

//  HGAppLive
http://wgz:wgz2024%@8.136.240.199:10101/r/HGAppLive.git

退出登录

    [[HGAccountManager manager] removeLoginCache];

    [[NSUserDefaults standardUserDefaults] removeObjectForKey:@"AppToken"];
    [[NSUserDefaults standardUserDefaults]synchronize];
    [APPDELEGATE setRootViewController];

- AI超级销售--盘活  HGAppLive
- 黑谷AI 2.0对应 AI获客  HGAppCatchCst
 - HGAIHKViewController


- AI会议秘书
- AI人才猎手

/Users/wuguizhao/Documents/HG-supersales-live/HGApp/heygood-video-ios/HGApp/HGPrefixHeader.pch Build input file cannot be found: '/Users/wuguizhao/Documents/HG-supersales-live/HGApp/heygood-video-ios/HGApp/HGPrefixHeader.pch'. Did you forget to declare this file as an output of a script phase or custom build rule which produces it?


HG_LoginVC 区分
HGMainTabBarController *tabBar
// 会议秘书

            HGMeetingTabBarController *tabBar = [[HGMeetingTabBarController alloc] initWithRecordingIndex:0];

            - HGRecordingPageVC 隐藏返回按钮

# 4.25
榜单类型错误
分享标签

 Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'Invalid update: invalid number of rows in section 0. The number of rows contained in an existing section after the update (18) must be equal to the number of rows contained in that section before the update (14), plus or minus the number of rows inserted or deleted from that section (1 inserted, 0 deleted) and plus or minus the number of rows moved into or out of that section (0 moved in, 0 moved out).

自定义xib View
```objc
- (void)commonInit {
    // 加载 xib 文件
    UIView *view = [[[NSBundle mainBundle] loadNibNamed:@"HGShareRecordTableSubView" owner:self options:nil] firstObject];
  }
```

# 4.24
Plank 14s
tap to start

1、样式换几个按钮、点击事件、逻辑
2、增加用法介绍文字
3、存储最长时间记录

let bellImage = UIImage(systemName: "bell")
铃铛
let calendarImage = UIImage(systemName: "calendar")
个日历图标
let flagImage = UIImage(systemName: "flag")
旗帜图标
let personImage = UIImage(systemName: "person.crop.circle")
人图标
let heartImage = UIImage(systemName: "heart.fill")
红色心形

# 4.23
- 录音统计规则调整：
暂停时5秒没到要把差值上报上去，然后继续之后就有开始继续5秒上报一次，视频播放结束之后跟暂停一样的的处理
- 获取录音类型列表接口替换
- 添加记录接口入参修改、联调
- 分享标签调整
- 增加总阅读时长显示


- 输入框撑开高度
textView scrollenable = no;
HGBusinessInformationPageListCell
- (CGFloat)tableView:(UITableView *)tableView heightForRowAtIndexPath:(NSIndexPath *)indexPath{
    return  UITableViewAutomaticDimension;
}



# 4.22
git add -A && git commit -m "添加大文件"
git puh

# 4.19

view切换

```objc
- (void)addSwitchView {
    [self.view addSubview:self.teamView];
    // 在上
    [self.view addSubview:self.departView];
}

- (void)deaprtViewPushToTeamView:(id) sender {
    //departView push到 teamView的效果
    [UIView animateWithDuration:0.3 animations:^{
        CGRect teamViewFrame = self.teamView.frame;
        teamViewFrame.origin.x = 0;
        self.teamView.frame = teamViewFrame;
        [self.view bringSubviewToFront:self.teamView]; // 将teamView置于最前
    }];
}

- (void)teamViewPopToDeaprtView:(id) sender {
    // teamView pop  的效果
    [UIView animateWithDuration:0.3 animations:^{
        CGRect teamViewFrame = self.teamView.frame;
        teamViewFrame.origin.x = SCREEN_WIDTH;
        self.teamView.frame = teamViewFrame;
    } completion:^(BOOL finished) {
        [self.view bringSubviewToFront:self.departView]; // 将departView置于最前
    }];
}

-(UIView *)teamView {
    if (!_teamView) {
        _teamView = [[UIView alloc] initWithFrame:CGRectMake(SCREEN_WIDTH, 150, SCREEN_WIDTH, 300)];
        _teamView.backgroundColor = [UIColor redColor];
        UITapGestureRecognizer * tap = [[UITapGestureRecognizer alloc] initWithTarget:self action:@selector(teamViewPopToDeaprtView:)];
        [_teamView addGestureRecognizer:tap];
    }
    return _teamView;
}

-(UIView *)departView{
    if (!_departView) {
        _departView = [[UIView alloc] initWithFrame:CGRectMake(0, 150, SCREEN_WIDTH, 300)];
        _departView.backgroundColor = [UIColor greenColor];
        UITapGestureRecognizer * tap = [[UITapGestureRecognizer alloc] initWithTarget:self action:@selector(deaprtViewPushToTeamView:)];
        [_departView addGestureRecognizer:tap];
    }
    return _departView;
}

```
```objc  
/// 判断是否是html字符串
- (BOOL)isHtmlString:(NSString *)htmlString {
    // 1
    NSString *htmlRegex = @"^<.*";
//    NSString *htmlRegex = @"<[^>]+>";;
    //@"<([A-Za-z][A-Za-z0-9]*)\\b[^>]*>(.*?)</\\1>";
    NSPredicate *htmlTest = [NSPredicate predicateWithFormat:@"SELF MATCHES %@", htmlRegex];
    BOOL isHTML = [htmlTest evaluateWithObject:htmlString];
    return isHTML;
}
```
# 4.18
```objc
- (void)switchViews {
    [UIView transitionWithView:self.view duration:0.5 options:UIViewAnimationOptionTransitionFlipFromLeft animations:^{
        view1.hidden = !view1.hidden;
        view2.hidden = !view2.hidden;
    } completion:nil];
}
```
```objc
- (void)showView1WithPopAnimation {
    [UIView transitionFromView:view2 toView:view1 duration:0.5 options:UIViewAnimationOptionTransitionFlipFromRight completion:nil];
}
```
# 4.16
Recording ranking list
HGAccountTypeSalesman 销售类型
HGAccountType accountType = [HGAccountManager manager].accountType;

cell ： HGRecordingPageSubTableViewCell
tag_checkBox_nor
SelectIcon 3


## Q:
我要在应用扩展 SampleHandler类里- (void)processSampleBuffer:(CMSampleBufferRef)sampleBuffer withType:(RPSampleBufferType)sampleBufferType拿到CMSampleBufferRef数据后
怎么->直播流->火山

开始直播 视频流
暂停
- (void)broadcastPaused

录制过程不断输出视频流
SampleHandler
```objc
- (void)processSampleBuffer:(CMSampleBufferRef)sampleBuffer withType:(RPSampleBufferType)sampleBufferType
```

```swift
- (void)processSampleBuffer:(CMSampleBufferRef)sampleBuffer withType:(RPSampleBufferType)sampleBufferType {
    switch (sampleBufferType) {
        case RPSampleBufferTypeVideo:
            // Handle video sample buffer
            // 得到YUV数据
            // 1、如果是会议 屏幕共享 -> processSampleBuffer
            // 2、写入本地文件 之后上传
```


#pragma mark - 屏幕分享 tap事件
-(void)screenShareViewHandleTap:(id) sender {
    static NSDate *lastTapTime;
    if (lastTapTime) {
        NSTimeInterval timeInterval = [[NSDate date] timeIntervalSinceDate:lastTapTime];
        if (timeInterval < 1.5) {
            // 点击间隔小于1.5秒，不执行操作
            return;
        }
    }

    [self isTopAndBottomBarHiddenOrShow];

    if (self.navViewTopConstraint.constant == 0) {
        [self.shareTapTimer startTimer];
    } else {
        [self.shareTapTimer stopTimer];
    }

    // 更新上次点击的时间
    lastTapTime = [NSDate date];
}

# 4.15
会议操作栏显示隐藏动画优化、全屏时字幕显示完善、
FFMpeg
音视频转码：将音频或视频文件从一个格式转换为另一个格式，例如将MP4视频转换为AVI格式或将音频从MP3转换为AAC格式。

媒体剪辑和拼接：从一个或多个音视频文件中提取特定的片段，并将它们合并成一个单独的文件。

视频编解码：使用不同的视频编解码器对视频进行编解码，以改变视频的压缩格式、分辨率、帧率和比特率。

音频处理：应用特定的音频滤镜和效果，如音频增益、降噪、混音等。

媒体信息提取：从音视频文件中提取元数据（如时长、分辨率、编解码器等）和流信息。

视频截图和缩略图生成：从视频中提取静态截图或生成视频缩略图。

实时音视频处理：通过FFmpegKit，你可以对实时音视频流进行处理，例如实时流媒体传输、实时音视频处理和实时转码等。

- 执行异步方法 FFmpegKit.executeAsync传入

##### 使用 -vf 参数可以在FFmpegKit中执行各种强大的视频滤镜操作。以下是一些常见的视频处理操作：

缩放（Scale）：调整视频的尺寸，可以按比例缩放或指定具体的宽度和高度。

旋转（Rotate）：将视频顺时针或逆时针旋转指定的角度。

裁剪（Crop）：从视频中提取指定区域的内容，去除周围不需要的部分。

滤镜（Filter）：应用各种视频滤镜来改变视频的外观和效果，如亮度、对比度、饱和度调整，色彩转换等。

帧率调整（Frame Rate Adjustment）：改变视频的帧率，可以加速或减慢视频的播放速度。

混流（Overlay）：将多个视频流合并到单个输出流中，可以实现图片水印、字幕等效果。

转码（Transcoding）：将视频从一个编码格式转换为另一个编码格式，如将MP4转换为AVI或将H.264转换为H.265。

视频编解码（Video Codec）：更改视频的编码方式，选择不同的视频编解码器以优化视频压缩和质量。

视频分割（Segmentation）：将视频分割成多个片段，可以按时间、大小或关键帧进行分割。

视频拼接（Concatenation）：将多个视频文件连接在一起，形成一个单一的视频文件。

##### 使用 -af 参数可以在FFmpegKit中执行各种强大的音频滤镜操作。以下是一些常见的音频处理操作：

音频增益（Volume）：调整音频的音量，可以增加或减小音频的音量级别。

声道操作（Channel Manipulation）：改变音频的声道布局，包括合并、拆分、交换声道等。

音频混音（Audio Mixing）：将多个音频流混合在一起，创建一个包含多个音频源的混合音频。

音频剪辑（Audio Clipping）：截取音频的特定片段，提取所需的部分，去除不需要的部分。

音频速度调整（Audio Speed Adjustment）：改变音频的播放速度，可以加速或减慢音频的播放速度。

音频变调（Audio Pitch Shifting）：改变音频的音调，使其高或低于原始音调。

音频混响（Audio Reverb）：为音频添加混响效果，改变音频的空间感和环境氛围。

音频降噪（Audio Noise Reduction）：减少音频中的背景噪音，提高音频的清晰度和质量。

音频格式转换（Audio Format Conversion）：将音频从一种格式转换为另一种格式，如MP3转换为AAC。

音频合成（Audio Synthesis）：通过合成算法生成音频信号，如生成音乐、声效等。

# 4.12
会议页面
HGMutiRoomVC
操作栏显示时 隐藏
上传单图
HG_VM upLoadImage

```objc
- (UIImage *)captureScreenshot {
    CGSize imageSize = UIScreen.mainScreen.bounds.size;
    UIGraphicsBeginImageContextWithOptions(imageSize, NO, 0);
    CGContextRef context = UIGraphicsGetCurrentContext();

    for (UIWindow *window in UIApplication.sharedApplication.windows) {
        CGContextSaveGState(context);
        CGContextTranslateCTM(context, window.center.x, window.center.y);
        CGContextConcatCTM(context, window.transform);
        CGContextTranslateCTM(context, -window.bounds.size.width * window.layer.anchorPoint.x, -window.bounds.size.height * window.layer.anchorPoint.y);

        if ([window respondsToSelector:@selector(drawViewHierarchyInRect:afterScreenUpdates:)]) {
            [window drawViewHierarchyInRect:window.bounds afterScreenUpdates:YES];
        } else {
            [window.layer renderInContext:context];
        }

        CGContextRestoreGState(context);
    }

    UIImage *screenshotImage = UIGraphicsGetImageFromCurrentImageContext();
    UIGraphicsEndImageContext();

    return screenshotImage;
}

dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
    UIImage *screenshotImage = [self captureScreenshot];

    dispatch_async(dispatch_get_main_queue(), ^{
        // 在主线程中使用截图结果
        // ...
    });
});

```

# 4.11

        make.left.greaterThanOrEqualTo(self).offset(6); // 最宽时距离父视图左边至少10像素
        make.right.lessThanOrEqualTo(self).offset(-6); // 最宽时距离父视图右边至少10像素
        make.width.greaterThanOrEqualTo(@(50)); // 最窄时宽度至少为50像素
# 4.10

#### 全屏时 topBar的view
SJVideoPlayerPresentView -> SJEdgeControlLayer
顶部 SJVideoPlayerControlMaskView -> SJEdgeControlButtonItemAdapter


    SJEdgeControlButtonItem *backItem = [_player.defaultEdgeControlLayer.bottomAdapter itemForTag:SJEdgeControlLayerTopItem_Back];
    [NSNotificationCenter.defaultCenter addObserver:self selector:@selector(itemActionDidSelectedBack:) name:SJEdgeControlButtonItemPerformedActionNotification object:backItem];


字幕
HGMeetingPageController
SJVideoPlayer
```objc
#import <SJBaseVideoPlayer/SJVideoPlayerURLAsset+SJSubtitlesAdd.h>
    // 1. 创建资源
     SJVideoPlayerURLAsset *asset = [SJVideoPlayerURLAsset.alloc initWithURL:URL];
     // 2. 设置资源的字幕
     asset.subtitles = @[[SJSubtitleItem.alloc initWithContent:@"我的故事" range:SJMakeTimeRange(start, duration)],                         [SJSubtitleItem.alloc initWithContent:@"从这里开始" range:SJMakeTimeRange(start, duration)]];
     // 3. 进行播放, 字幕将在相应的时机自动显示
     _player.URLAsset = asset;
     ///
///     // 以下是更多设置
///     _player.subtitleBottomMargin = 22.0;
///     _player.subtitleHorizontalMinMargin = 22.0;
///     _player.subtitlePopupController.view.backgroundColor = [UIColor colorWithWhite:0 alpha:0.8];
///     _player.subtitlePopupController.view.layer.cornerRadius = 5;
///     _player.subtitlePopupController.contentInsets = UIEdgeInsetsMake(12, 22, 12, 22);
///

/// 控制

SJVideoPlayerControlLayerDelegate

- (void)subtitleButtonTapped:(UIButton *)sender {
    // 在按钮点击事件中，通过代理方法通知播放器控制字幕的显示和隐藏
    if ([self.delegate respondsToSelector:@selector(controlLayerNeedDisappear:)]) {
        [self.delegate controlLayerNeedDisappear:self];
    } else if ([self.delegate respondsToSelector:@selector(controlLayerNeedAppear:)]) {
        [self.delegate controlLayerNeedAppear:self];
    }
}
```

```objc

// 更新字幕
- (void)updatePlayerSubtitle {
    NSDictionary *attributes = @{
        NSForegroundColorAttributeName: [UIColor whiteColor],
        NSFontAttributeName: [UIFont systemFontOfSize:16.0]
    };
    NSArray *array =  @[[[SJSubtitleItem alloc] initWithContent:[[NSAttributedString alloc] initWithString:@"X故事准备开始" attributes:attributes] start:121 end:130],
                        [[SJSubtitleItem alloc] initWithContent:[[NSAttributedString alloc] initWithString:@"X结束了" attributes:attributes] start:130 end:139],
                        [[SJSubtitleItem alloc] initWithContent:[[NSAttributedString alloc] initWithString:@"X在这个示例中，我们创建了一个名为SubtitleView的自定义视图类，并在初始化方法中添加了一个UILabel作为字幕的容器。setSubtitle:方法用于设置字幕内容，showSubtitle和hideSubtitle方法用于控制字幕的显示和隐藏。" attributes:attributes] start:140 end:160],
                        [[SJSubtitleItem alloc] initWithContent:[[NSAttributedString alloc] initWithString:@"X结束了read-side closed故事……" attributes:attributes] start:161 end:220],
    ];
    // 创建新的URLAsset对象，并将新的字幕数组赋值给subtitles属性
    SJVideoPlayerURLAsset *newAsset = [[SJVideoPlayerURLAsset alloc] initWithURL:self.urlAsset.mediaURL startPosition:self.urlAsset.startPosition];
    newAsset.subtitles = array;
    self.urlAsset = newAsset;
    // 更新播放器的URLAsset
    self.player.URLAsset = newAsset;

}
```

```
 #import <SJBaseVideoPlayer/SJDanmakuItem.h>

        // 创建一条弹幕
         SJDanmakuItem *item = [SJDanmakuItem.alloc initWithContent:[NSAttributedString sj_UIKitText:^(id<SJUIKitTextMakerProtocol>  _Nonnull make) {
            make.append( @"我是一条弹幕消息" );
             make.font([UIFont boldSystemFontOfSize:16]);
            make.textColor(UIColor.whiteColor);
             make.stroke(^(id<SJUTStroke>  _Nonnull make) {
                 make.color = UIColor.blackColor;
                 make.width = -1;
             });
         }]];

         // 发送一条弹幕, 弹幕将自动显示
         [self.player.danmakuPopupController enqueue:item];
```
# 4.9
悬浮试图 HGFloatButton

- HGScreenShareView 分享的屏幕禁止缩放
- 显示操作栏定时器 shareTapTimer

# 4.8
// 多人会议
HGMutiRoomVC
禁用滚动
[self.screenContentView addGestureRecognizer:self.pinchGesture];

// 时长
    RecordAdditions *additions = [RecordAdditions modelWithJSON:model.additions];

// 数据请求loading
[JHToastManager show];

#### 字幕滚动view
```objc
//
//  HGTextScrollView.h
//  HGApp
//
//  Created by 吴桂钊 on 2024/4/8.
//

#import <UIKit/UIKit.h>

NS_ASSUME_NONNULL_BEGIN

@interface HGTextScrollView : UIView
// 最新内容
@property(nonatomic, strong) NSString *lastContent;
@end

@interface HGTextScrollTableCell: UITableViewCell
@property(nonatomic, strong) UILabel *contentLabel;
@end

NS_ASSUME_NONNULL_END

```
```objc
//
//  HGTextScrollView.m
//  HGApp
//
//  Created by 吴桂钊 on 2024/4/8.
//

#import "HGTextScrollView.h"

@interface HGTextScrollView ()<UITableViewDelegate,UITableViewDataSource>
@property(nonatomic, strong) UITableView *tableView;
@property(nonatomic, strong) NSMutableArray *dataSource;
@end

@implementation HGTextScrollView
- (instancetype)initWithCoder:(NSCoder *)coder{
    self = [super initWithCoder:coder];
    if (self) {
        [self setupUI];
    }
    return self;
}

- (void)encodeWithCoder:(nonnull NSCoder *)coder {

}

- (instancetype)initWithFrame:(CGRect)frame{
    self = [super initWithFrame:frame];
    if (self) {
        [self setupUI];
    }
    return self;
}

-(void)setLastContent:(NSString *)lastContent{
    _lastContent = lastContent;
    [self.dataSource insertObject:_lastContent atIndex:0];
    [self.tableView insertRow:0 inSection:0 withRowAnimation:UITableViewRowAnimationTop];
//    [self.tableView reloadData];
}

- (void)setupUI {
    self.dataSource = [NSMutableArray array];
    [self addSubview:self.tableView];
    [self.tableView mas_makeConstraints:^(MASConstraintMaker *make) {
        make.edges.equalTo(self).insets(UIEdgeInsetsMake(0, 0, 0, 0));
    }];
    self.tableView.separatorStyle = UITableViewCellSeparatorStyleNone;
}

- (nonnull UITableViewCell *)tableView:(nonnull UITableView *)tableView cellForRowAtIndexPath:(nonnull NSIndexPath *)indexPath {
    HGTextScrollTableCell *cell = [tableView dequeueReusableCellWithIdentifier:@"HGTextScrollTableCell" forIndexPath:indexPath];
    cell.selectionStyle = UITableViewCellSelectionStyleNone;
    cell.contentLabel.text = self.dataSource[indexPath.row];
    return cell;
}

- (NSInteger)tableView:(nonnull UITableView *)tableView numberOfRowsInSection:(NSInteger)section {
    return self.dataSource.count;
}

- (UITableView *)tableView {
    if (!_tableView) {
        _tableView = [[UITableView alloc] initWithFrame:CGRectZero style:UITableViewStylePlain];
        _tableView.delegate = self;
        _tableView.dataSource = self;
//        _tableView.estimatedRowHeight = 30;
        [_tableView registerClass:[HGTextScrollTableCell class] forCellReuseIdentifier:@"HGTextScrollTableCell"];
        _tableView.backgroundColor = [UIColor clearColor];
        _tableView.transform = CGAffineTransformMakeScale(1, -1);
    }
    return _tableView;
}

@end


@implementation HGTextScrollTableCell

-(instancetype)initWithFrame:(CGRect)frame {
    self = [super initWithFrame:frame];
    return self;
}

-(instancetype)initWithStyle:(UITableViewCellStyle)style reuseIdentifier:(NSString *)reuseIdentifier {
    self = [super initWithStyle:style reuseIdentifier:reuseIdentifier];
    if (self) {
        // cell旋转
        self.contentView.transform = CGAffineTransformMakeScale(1, -1);
    }
    return self;
}

-(void)layoutSubviews {
    [super layoutSubviews];
    self.contentView.backgroundColor = RGBA(0, 0, 0, 0.4);
    [self.contentLabel mas_makeConstraints:^(MASConstraintMaker *make) {
        make.edges.equalTo(self.contentView).insets(UIEdgeInsetsMake(6, 50, 6, 15));
    }];
}

- (UILabel *)contentLabel {
    if (_contentLabel == nil) {
        _contentLabel = [[UILabel alloc] init];
        _contentLabel.font = [UIFont systemFontOfSize:14];
//        _contentLabel.adjustsFontSizeToFitWidth = YES;
        _contentLabel.textColor = [UIColor redColor];
        _contentLabel.numberOfLines = 2;
        [self.contentView addSubview:_contentLabel];
    }
    return _contentLabel;
}

@end

```
# 4.7
18030251115 ->
HGAddDYAccountViewController
新增抖音号

# 4.3
点赞评论设置页ipad崩溃
UIAlertController  的 UIAlertControllerStyleActionSheet 需要 UIAlertControllerStyleAlert

# 4.2
// log-url转义后加载

// 刷新通知 GoJobReload
```objc
HGJobModel*model=[self.dataArray objectAtIndex:indexPath.section];
HGJobDetailPageVc *vc = [[HGJobDetailPageVc alloc] init];
vc.jobModel = model;
[self.navigationController pushViewController:vc animated:YES];
```
```objc
            // 富文本实现第二行空格
           NSMutableAttributedString *attributedText = [[NSMutableAttributedString alloc] initWithString:showTime];
           NSMutableParagraphStyle *paragraphStyle = [[NSMutableParagraphStyle alloc] init];
           paragraphStyle.firstLineHeadIndent = 0;
           // n个中文空格的宽度
           paragraphStyle.headIndent = self.timeLabel.font.pointSize * 6;
           paragraphStyle.alignment = NSTextAlignmentLeft;
           paragraphStyle.lineSpacing = 6;
           [attributedText addAttribute:NSParagraphStyleAttributeName value:paragraphStyle range:NSMakeRange(0, attributedText.length)];
           self.timeLabel.attributedText = attributedText;
```

# 4.1
未完成 miniProgram-shop-icon
私发编辑：
HGPrivateContentChatVC
时间选择器类型切换、获取门店信息、新增小程序类型、新增修改接口联调、列表时间显示修改；


- 重复请求
[[GCDTimerManager sharedInstance] scheduleGCDTimerWithName:@"refleshDialogListUI"

/weixin/hgvWeixinUnreadDialog/getNotRealMessage

# 3.30
- 人才列表列表展示
- 私发编辑 cell -HGPrivateContentWechatMiniprogramTableCell

- 私发编辑列表页面：HGPrivateContentPageSubVC
-- HGPrivateContentPageSubTableViewCell

- self.titleBtn SG_imageLocationStyle 会议详情标题
NSString *trimmedString = [originalString stringByTrimmingCharactersInSet:[NSCharacterSet whitespaceCharacterSet]];

# 3.29
私发编辑页面：发送时间选择时间UI功能完成、待接口；
HGPrivateContentChatVC
tag
self.datePickerView.pickerHeaderView = self.pickerHeaderView


1. 会议秘书 复制视频副本 **完成**
- HGRecordingPageSubVC
-- HGRecordingPageSubTableViewCell
【3-会议秘书（增加复制副本）】
https://www.tapd.cn/56897205/prong/stories/view/1156897205001008040
2.  todo
HGGPTViewController switchIndustries
HGSwitchIndustriesVC
【【AI财务功能】现在进入AI财务页面默认行业为空，需记忆上次所选行业，再次进入默认选择对应行业】
https://www.tapd.cn/56897205/prong/stories/view/1156897205001006239



# 3.28
完成人才猎手提测
简历设置页面重构
通知刷新


# 3.27
文档解析器内存问题优化；上传后延迟跳转到会议秘书；
人才猎手 账号密码：18064431783  431783
公司地址接口完成：问题：没有选中。vlaue却有值

地址picker：
##1、FormCityPicker
   - provinceName
        - citylist cityName
        - arealist areaName

##2、BRAddressPickerView

```objc
BRAddressPickerView *p = [[BRAddressPickerView alloc] init];
self.cityPickerView = p;
p.pickerMode = BRAddressPickerModeArea;
p.resultBlock = ^(BRProvinceModel * _Nullable province, BRCityModel * _Nullable city, BRAreaModel * _Nullable area) {

    NSArray *array = @[@"省",@"自治区",@"特别行政区",@"市",@"区",@"县"];
    NSString *provinceStr = province.name;
    NSString *cityStr = city.name;
    NSString *areaStr = area.name;

    for (NSString *unit in array) {
        if ([provinceStr containsString:unit]) {
            NSRange r = [provinceStr rangeOfString:unit];
            provinceStr = [provinceStr substringToIndex:r.location];
        }

        if ([cityStr containsString:unit]) {
            NSRange r = [cityStr rangeOfString:unit];
            cityStr = [cityStr substringToIndex:r.location];
        }

        if ([areaStr containsString:unit]) {
            NSRange r = [areaStr rangeOfString:unit];
            areaStr = [areaStr substringToIndex:r.location];
        }
    }

    if ([provinceStr isEqualToString:@"台湾"] ||[provinceStr isEqualToString:@"香港"] ||[provinceStr isEqualToString:@"澳门"]) {

        areaStr = provinceStr;
    }
    self.province = provinceStr;
    self.area = areaStr;
    if ([areaStr isEqualToString:@"所有"] || areaStr.length == 0) {

        self.area = cityStr;
    }
    [self saveCity];
//        [self requestProviceWithArea:self.city];
};
[p show];
```




# 3.26
./upload.sh -d "提测ipad适配" HGApp\ 2024-03-05\ 15-53-03/

fastlane使用brew安装成功；gem重装pods；ruby版本更新；解决brew-ruby无法更新的问题；

保存文档接口：
        gptKnowledgeArticleSaveWithCategoryId
heygood-video/gpt/knowledge/article/saveText

### NSAttributedString 转为 html字符串
        NSError *error = nil;
        NSData *htmlData = [contentAttributedString dataFromRange:NSMakeRange(0, contentAttributedString.length) documentAttributes:@{NSDocumentTypeDocumentAttribute: NSHTMLTextDocumentType} error:&error];
        if (htmlData && !error) {
            NSString *htmlString = [[NSString alloc] initWithData:htmlData encoding:NSUTF8StringEncoding];
            // NSAttributedString 转成 html字符串
            [dic setObject:htmlString forKey:@"content"];
        }

### html字符串 转为 NSAttributedString
NSString *htmlString = @"<b>Bold Text</b> <i>Italic Text</i> <u>Underline Text</u>";

NSData *htmlData = [htmlString dataUsingEncoding:NSUTF8StringEncoding];
NSDictionary *options = @{NSDocumentTypeDocumentAttribute: NSHTMLTextDocumentType};

NSAttributedString *attributedString = [[NSAttributedString alloc] initWithData:htmlData options:options documentAttributes:nil error:nil];

### 详情页 HGRecordPlayTranscriptSubVC

1. 文件点击分享，利用webView解析拿到文档的字符串和html字符串
   -->
2. 接下来，调用heygood-video/gpt/knowledge/article/saveText接口（html字符串传入content字段），上传到会议秘书文档
   -->
3. 完成上传后列表进详情，通过transcript字段判断是不是html字符串，区分普通文本详情还是html详情。

4.详情页判断是html详情的转换为富文本显示。


#### pdf获取文字
#import <PDFKit/PDFKit.h>

// 在加载PDF文件的地方，可以使用以下代码来获取文档中的文字
NSURL *pdfURL = [NSURL fileURLWithPath:@"path_to_your_pdf_file"];
PDFDocument *pdfDocument = [[PDFDocument alloc] initWithURL:pdfURL];

if (pdfDocument) {
    NSMutableString *extractedText = [NSMutableString string];

    for (NSInteger pageIndex = 0; pageIndex < pdfDocument.pageCount; pageIndex++) {
        PDFPage *page = [pdfDocument pageAtIndex:pageIndex];

        NSString *pageText = [page string];
        if (pageText) {
            [extractedText appendString:pageText];
        }
    }

    NSLog(@"Extracted Text: %@", extractedText);
} else {
    NSLog(@"Failed to load PDF document.");
}
