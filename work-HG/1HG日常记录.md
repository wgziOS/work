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

- 其他账号
测试版 18030251115  密码 251115

# 7 16
word_delete_icon
http://view.xdocin.com/xdoc
本地搜索
NSPredicate *predicate = [NSPredicate predicateWithBlock:^BOOL(HGFriendModel *evaluatedObject, NSDictionary *bindings) {
            return [evaluatedObject.friendName containsString:searchText];
        }];
        self.filteredFriends = [self.dataMuArray filteredArrayUsingPredicate:predicate];


JXPagerViewDelegate,JXCategoryViewDelegate

淡蓝色   背景灰色
EFF4FF  f1f1f1
字体 999999 灰色  037afe 蓝色


swift 的项目，默认进入是登录页面，登录后展示一个tabbarController，下的四个页面。

# 8

        contentView.layer.cornerRadius = 9
        contentView.layer.maskedCorners = [.layerMinXMinYCorner, .layerMaxXMinYCorner]


oc代码实现一个录音机的功能：
1、有暂停有恢复录制有停止的功能；
2、录音机实时录制的时候5秒回调出去录音数据；
3、结束录音的时候回调完整的录音数据；
两个线程同时
一个线程读录音机数据放进队列，另个线程从队列取数据给引擎


# 7
账号 13599580520
 @"1455744458007883777" @"1455776332805681154"
jumpNextExcelWith 蒋书容（总监） departId:1455744458007883777
jumpNextExcelWith 汤锦良美业 departId:1455776332805681154
backUpLevel - departId:1455776332805681154 level:1

// 将 view1 移到最前面
[self.view bringSubviewToFront:view1];

// 将 view2 移到最后面
[self.view sendSubviewToBack:view2];


getSaleDepartManagerTaskListWithDepartId

参考抖音一比一 要比抖音更牛逼
let input = HGWxCrowdAutoFetchingModel()
        input.autoOpenWxCrowdAdd = sender.isSelected ? 0 : 1
        input.wxId = currentModel.wxId;
recruitdetail 右箭头
recruitArrow 下箭头


    [self.tableView registerNib:[UINib nibWithNibName:@"HGChooseRankTypeSectionView" bundle:nil] forHeaderFooterViewReuseIdentifier:@"HGChooseRankTypeSectionView"];


    HGChooseRankTypeSectionView *sectionView = [tableView dequeueReusableHeaderFooterViewWithIdentifier:@"HGChooseRankTypeSectionView"];

categroy_add_blue_icon
category_check_icon

unselect_circle
recording_exam_select

    [self.moitoringButton setOCStyleWithStyle:@(2)
                                       margin:6
                                    imageSize:CGSizeMake(18, 18)
                                   marginEdge:UIEdgeInsetsMake(0, 0, 0, 0)
                                 distribution:@(1)
    ];
    [self.moitoringButton setOCFontWithFont:HGMediumFont(12)];




UIButton *setBtn = [UIButton buttonWithType:UIButtonTypeCustom];
[setBtn setImage:[UIImage imageNamed:@"job_mian_set"] forState:UIControlStateNormal];
setBtn.frame = CGRectMake(0, 0, 40, 40);
[setBtn setTitle:@"设置" forState:UIControlStateNormal];
setBtn.titleLabel.font = Font(12);
[setBtn setTitleColor:[UIColor colorWithHexString:@"#999999"] forState:UIControlStateNormal];
[setBtn addTarget:self action:@selector(touchSetBtn) forControlEvents:UIControlEventTouchUpInside];
[setBtn SG_imageLocationStyle:SGImageLocationStyleTop spacing:2];

NSMutableArray * datas = [NSMutableArray array];
        [self.defaultAddList enumerateObjectsUsingBlock:^(HGDefaultTypeTableEnvelop * _Nonnull obj, NSUInteger idx, BOOL * _Nonnull stop) {
            HGDefaultTypeTableEnvelop * temp = [[HGDefaultTypeTableEnvelop alloc] init];
            temp.id = obj.id;
            temp.code = obj.code;
            temp.name = obj.name;
            temp.isSelected = @(NO);
            [obj.detailList enumerateObjectsUsingBlock:^(HGDefaultTypeTableEnvelop * _Nonnull subObj, NSUInteger idx, BOOL * _Nonnull stop) {
                subObj.isSelected = @(NO);
            }];
            temp.detailList = obj.detailList;
            [datas addObject:temp];
        }];


    var checkClosure: ((Bool, [String]) -> Void)?

    for (index, model) in leftDataSource.enumerated() {
        // 在这里使用 index 和 model
        print("Index: \(index), Model: \(model)")
    }


        CGRect cellRect = [self.tableView rectForRowAtIndexPath:indexPath];
        CGRect convertedRect = [self.tableView convertRect:cellRect toView:self.tableView.superview];

# 6.26
self.textView.layer.masksToBounds=YES;
  self.textView.layer.cornerRadius=5;
  self.textView.layer.borderColor=JHColorHex(0xEEEEEE).CGColor;
  self.textView.layer.borderWidth=1;

【页面拼接】【抖音拓客】开发抖音客户

# 6.26
hkb_checkBox_btn hkb_checkBox_btn_selected
self.store.ID
HGEmployeeListVC
 员工列表
 HGMeRequest *r = [[HGMeRequest alloc] init];
     [r shopEmployeeListWithShopId:self.shopInfo.ID
                           keyword:keyword
                           success:^(NSArray * _Nullable modelList, NSString * _Nullable message) {
         // ???: 什么鬼？分页是这么做的？
         self.dataMuArray = modelList.mutableCopy;
         [self.tableView reloadData];
         [self.tableView.mj_header endRefreshing];
         [self.tableView.mj_footer endRefreshing];

     } failure:^(NSError * _Nullable error) {
         [self.tableView.mj_header endRefreshing];
         [self.tableView.mj_footer endRefreshing];

     }];

   HGMeRequest *r = [[HGMeRequest alloc] init];
   [r getSelectedShopWithSuccess:^(HGShopInfo * _Nonnull shopInfo) {

       self.selectedShop = shopInfo;
       [self.titleButton setTitle:shopInfo.shopName forState:UIControlStateNormal];
       [self.titleButton SG_imageLocationStyle:SGImageLocationStyleRight spacing:6 imageLocationBlock:^(UIButton * _Nonnull button) {

       }];
   } failure:^(NSError * _Nullable error) {

   }];


   #import "TTPickerDateVc.h"
   #import "TTPickerStringVc.h"
   // 滚轮数据
   FormInputModel *_weekModel=[FormInputModel new];
    _weekModel.placeholder=@"请选择星期";
    _weekModel.picker_list = [@[@"周一",@"周二",@"周三",@"周四",@"周五",@"周六",@"周日"] mutableCopy];
    _weekModel.text = @"周一";
    _weekModel.value = @"1";


    [TTPickerStringVc showVc:self dateModel:model.weekModel pickerMode:BRStringPickerComponentSingle block:^(BRResultModel * _Nullable resultModel) {
            @Strongify(self);
            model.viewTimeType = 2;
            model.weekModel.text = resultModel.value;
            model.weekModel.value=@(resultModel.index+1).stringValue;
            indexModel.week=@(resultModel.index+1).stringValue;
            indexModel.weekText=resultModel.value;
            [model reloadData];
            [self reloadHealthyData];
        }];

# 6.26

window 层上 HGAILeftChatList HGAIOptimizationPromptView
HGCatchWXGroupFilterView

# 6.21
NSArray *permissionCodes = [HGAccountManager manager].moduleCodes;
if (![permissionCodes containsObject:@"syph"]) {

          [JHToastManager showInfoWithStatus:@"未购买，暂无权限" duration:0.5];
          return;
      }  


HGCatchWXGroupFilterView

HGHomeCustomerTableCell


# 6.18

var deleteClosure: (() -> Void)?


    public typealias DelectPhotoClosure = () -> Void

    var delectPhotoClosure: DelectPhotoClosure?

//    public typealias SwitchValueClosure = (_ isOn: Bool) -> Void
//
//    var switchValueClosure: SwitchValueClosure?
guard let closure = self.delectPhotoClosure else {
           return
       }
       closure()

Privacy - Location Always Usage Description
是否允许在使用过程中获取您的定位信息用于视频账号绑定操作

catch-own-customer

ViewBorderRadius(self.addWayTable, 4, 1, JHLineColor);


# 6.15
自动加微信设置、通讯录添加

# 6.14

bottomBtn_bg
HGAutoAddWxSettingViewController

CGRect cellFrame = [tableView rectForRowInSection:indexPath];

https://ai.xmheigu.com/report/report.html?userId=1792907476728909826

# 6.13
加计扣除项目联调

http://wgz:wgz2024%@8.136.240.199:10101/r/HGAppCatchCst-ios.git

HGAppLive
http://wgz:wgz2024%@8.136.240.199:10101/r/heygood-supersale-ios.git
# 6.12

自定义条形进度视图、样式参数可配

```objc
//进度条
       HGProgressView *progressView = [[HGProgressView alloc] initWithFrame:CGRectMake(30, 365, 150, 50)];
//    HGProgressView *progressView = [[HGProgressView alloc] init];

    //进度条边框宽度
    progressView.progerStokeWidth = 0.f;
    //背景边框颜色
    progressView.progerssStokeBackgroundColor = [UIColor greenColor];
    //进度条未加载背景
    progressView.progerssBackgroundColor = [UIColor redColor];
    //进度条已加载 颜色
    progressView.progerssColor = [UIColor orangeColor];
    progressView.insetPadding = 5;
    progressView.cornerRadius = 8;
    progressView.progerssCornerRadius = 20;

    [self.view addSubview:progressView];
//    [progressView mas_makeConstraints:^(MASConstraintMaker *make) {
//        make.top.left.equalTo(self.view).offset(20);
//        make.right.equalTo(self.view).offset(-20);
//        make.height.mas_equalTo(@50);
//    }];

    progressView.progress = 0.75;
    self.progressView = progressView;


    dispatch_after(dispatch_time(DISPATCH_TIME_NOW, (int64_t)(5 * NSEC_PER_SEC)), dispatch_get_main_queue(), ^{
        self.progressView.progress = 0.95;
    });
```
# 6.4
【抖音拓客】开发抖音客户、给客户发送私信、抖音基础设置 bug修复

# 5.29
修复上拉加载控件动画不居中的问题；
刷新控件类名不规范、
gif文件压缩大小

性别设置接口走swift类实现；
indicatorView适配ios13以上;
人才猎手代码增加注释、删除无用代码；

获客页面按钮渐变色改layer实现；


1.若干怪物的血量是正整数9，怪物血量变为0时判定死亡
2.玩家单次攻击可以对一个怪物造成一点伤害
3.怪物生命值削减到最大生命值一半时会对所有怪物造成一点伤害
给一个算法oc语言，输入一个整形数组9代表怪物的血量，求令所有怪物死亡的最少攻击次数。

NSMutableArray<NSNumber *> *monsterHP = [@[@9, @9, @9] mutableCopy];

次数 血量
5    4 9 9
6    3 8 8
9     0 5 5
10    0 4 5
11    0 3 4
14     0  0 1
15    0  0 0


编译器过期指令
__deprecated_msg("已废弃, 请使用 failureCallback");

# 5.27

优化HGReachability内监听对象可空逻辑;


```objc
```
# 5.24
HGTKRecordsViewController ->
绑定微信设置
HGAccountListViewController
vc.isWechat = YES;
 vc.isFromAIHK = YES;

 抖音基础设置  HGAccountListViewController
 vc.viewType = 1;
vc.isFromDouyinHuoke = YES;

- 转正
接入火山实时音视频SDK、实现多人语言会议

工作业绩结果描述（数据量化）

 1、完成【会议秘书】视频美颜、上传word转文本文档、上传视频增加黑边、复制副本、语音跳过空白片段、自定义字幕功能、录音分享及排行榜多期需求开发；
 2、完成【多人音视频会议】全屏显示、显示发言人等需求、解决了sdk多个方法不回调的问题；
 3、利用系统AVFoundation库完成自定义了音频音量设定阈值分析类，实现了音频音量阈值分析；
 4、完成【人才猎手】新增职位、工作地址选中多个需求开发解决人才猎手历史遗留问题，优化了人才猎手自定义列表的的表单类型、增加相应的注释，增加可维护性；
 5、完成【AI超级销售】精准线索、私信回复设置、抖音基础设置、人工介入设置、定时重复私发、短信拓客等多期需求开发；


- 工作态度和技能
1、我一直秉持着积极向上的工作态度，勇于承担责任，并且与团队成员友好沟通，保持良好的合作关系。
2、在技能方面，我熟练掌握iOS开发，精通Objective-C和Swift及Dart编程语言。此外，我在工作中拥有丰富的经验，熟悉业务开发流程。

- 价值观精神观落地
  我对公司的企业文化和价值观深感认同，并且努力将其融入到我的工作中，实现个人与公司的共同价值。
- 个人的优势
 1、我在iOS开发领域拥有8年的经验，并参与了多个大型App项目开发。
 2、在团队合作中，我善于与同事们密切合作，共同解决技术难题，提高项目的效率和质量。
 3、我对每个项目和任务都保持高度的责任心，并致力于按时交付高质量的工作成果。
 4、我持续关注最新的iOS开发技术和趋势，并将其应用到实际项目中。
- 个人需要提升方面
1、持续学习： 积极参与技术社区，关注最新的 iOS 开发技术和趋势，并通过在线课程、书籍和会议等方式不断提升自己的技术水平。
2、深入研究： 选择感兴趣的技术领域进行深入研究，并探索其在 iOS 开发中的应用潜力。
3、代码精进： 采用更严格的编码规范，编写更加健壮、可维护和易于理解的代码。积极参与代码审查，并向经验丰富的开发者学习最佳实践。
- 未来工作的方向和目标
1、深耕我的专业领域充满热情，我计划进一步探索最新的iOS开发技术，并将其应用于项目中，以提升公司产品的质量和竞争力。我将主动关注行业动态，并不断学习和实践，以保持在技术领域的前沿。
2、更深入地了解项目需求和团队成员的合作，我能够更好地协调资源，提高项目的执行效率和质量。我将积极与团队成员合作，共同营造一个良好的协作环境，以推动项目的成功。

# 5.23
工作业绩结果描述（数据量化）
这边罗列一下比较大的工作成果，其他小的就不一一罗列，具体如下：
一、业务层面的工作：
1. 完成会议秘书试题考核相关需求开发
2. 完成构建公司大脑第一个版本开发（基于总库 微信调试的基础上扩充出公司大脑第一个版本）
3. 完成AI财务第一个版本需求开发（基于微信调试的基础上扩充出AI财务）
4. 完成会议秘书评论的主体开发，在开发中优化了原有的bug以及性能。包括：跟读高亮多次遍历导致长按选择区间弹出菜单栏会自动消失的bug、摘要GPT转写实时缓存太耗费性能导致卡死的bug（优化为数据库存储）、优化火山引擎数据返回由原本的操作字典来实现数据的增、改优化为使用 model 来操作，增加可读性。
5. 完成会议秘书视频压缩需求开发，并将压缩封装成工具，便于后续使用。
6. 解决微信分享失败问题（由于universal Link 配置引起）。
7. 完成私发相关的需求开发
8. 完成私发标签管理通讯录、近三日好友以及对应的托管需求开发。
9. 完成AI超级销售-内部需求开发
10. 完成获客分店需求开发。

二、其他方面的工作：
1. 优化登录数据存储并将其封装为 HGAccountManager，由原本的每个数据单独存储优化为存储全部数据并以model的形式来调用，减少冗余代码、出错率，增加了可维护性、开发效率。
2. 梳理归纳了部分分类的代码，减少了重复的 api 10个以上。
3. 封装火山引擎调用，原本是使用的地方自己写一套，各自实现配置容易出现差错，封装后在有涉及到对应的需求开发的时候替换成封装的，后续就可以减少多处维护，目前如果全部替换可以减少3处的维护。
4. 封装音频播放器，用于评论，同个页面需要多个音频切换播放，原先暂无此功能（原先的录音只是单个页面无法满足），封装后该播放器支持单个、多个的音频播放，后续如果有类似的功能只需要直接调用即可。
5. 梳理项目中的TabBar标签栏，整理后减少5处以上的维护。
6. 修改 dev 环境的切换设置，增加弹窗支持动态修改ip，增加了本地联调的灵活性减少多次打包费时的问题。
工作态度和技能
工作态度：
个人认为自己的工作态度端正，积极向上，不推卸，能够主动承担，能够很好的与团队成员友好交流沟通。
技能：
1. 精通iOS开发，精通 Objective-C 开发，熟练应用 Swift 编程语言。
2. 有丰富的工作经验、以及业务开发经验。
价值观精神观落地
认同公司的企业文化以及公司的价值观。能够很好的适应公司文化，实现自身价值。
个人的优势
1. 有7年的 iOS 开发经验，有百万级日活跃的App开发经验。
2. 能够与团队成员密切合作，我们共同解决了一些技术难题，提高了项目的效率和质量。
3. 我对工作充满责任心，对每一个项目和任务都能够保持高度的执行力。
4. 在不断发展的科技行业，我始终保持学习和适应的态度。
5. 我善于分析和解决问题，成功解决了一些复杂的技术难题。
个人需要提升方面
1. 认识到技术领域变化迅速，致力于持续学习和深入了解最新的iOS开发技术和趋势，以确保我的技术水平保持在行业的前沿。
2. 希望提升我的项目管理技能，更好地协调团队工作、合理分配资源，确保项目按时交付且质量达到预期。
3. 进一步加强对代码质量的关注，采用更严格的编码规范，以确保我产生的代码更加健壮、可维护且易于理解。
4. 更深入地了解公司业务和产品，以便更好地将技术与业务需求结合起来，从而更好地为公司创造价值。
未来工作的方向和目标
1. 进一步深入我的专业领域，探索iOS开发的最新技术，并在项目中应用这些技术，以提高公司产品的质量和竞争力。
2. 加强项目管理技能，争取更多的机会参与项目规划和执行，同时积极与团队成员合作，创造协作愉快的工作环境。
3. 更深入地了解公司的产品和业务，以便更好地理解技术与业务之间的关系，为公司的产品提供更加全面的支持。

```objc
- (void)createProgressLabel
{
    NSString * content = @"显示一句话，看着像歌词";
    _progressLabel2 = [[HGProgressLabel alloc] initWithFrame:CGRectMake(0, 70, SCREEN_WIDTH, 50)];
    _progressLabel2.textAlignment = NSTextAlignmentCenter;
    _progressLabel2.seconds = 13;// 几秒走完进度
    UIFont *cusFont = [UIFont fontWithName:@"MFDianHei_Noncommercial-ExBold" size:23.0];
    _progressLabel2.attributedText = [content yg_makeAttributed:^(YGAttributedMaker *make) {
        make
            .font(cusFont)
            .foregroundColor([UIColor whiteColor])
            .strokeWidth(-5.0)
            .strokeColor([UIColor blackColor])
            .allRange();
    }];
    _progressLabel2.foregroundAttributedText = [content yg_makeAttributed:^(YGAttributedMaker *make) {
        make
            .font(cusFont)
            .foregroundColor([UIColor redColor])
            .strokeWidth(-5.0)
            .strokeColor([UIColor blackColor])
            .allRange();
    }];
    [self addSubview:_progressLabel2];
    [self.progressLabel2 startProgress];

}
```

# 5.21
添林
http://192.168.80.200:8088/

如果在榜单的 isChart ==1 的时候 再次分享的时候 默认勾选同步榜单

录音类型切换 回到列表

通知name
HGRankStatistiscFilterNotification

# 5.20
arc4random()%9

https://github.com/Augustyniak/RATreeView/issues/274

pod "RATreeView", "~> 2.1.2"

// pod 'RATreeView', :git => 'https://github.com/mgfjxxiexiaolong/RATreeView'

+ (RATreeViewStyle)treeViewStyleForTableViewStyle:(UITableViewStyle)tableViewStyle
{
  switch (tableViewStyle) {
    case UITableViewStylePlain:
      return RATreeViewStylePlain;
    case UITableViewStyleGrouped:
      return RATreeViewStyleGrouped;
  }
}

需要实现一个oc语言的一个多级展开的列表：左侧有勾选按钮，中间有当前title的label,右侧有展开收起的icon。
至少支持5级数据；需要有初始化指定选中某一项的功能，选中的项如果有父级那父级需要时展开状态；需要有重置选中的功能。




# 5.17
task：
- 主管总监权限判断接口
- 全屏倍数

会议秘书字幕、全文复制、榜单；视频全屏倍数功能；登录销售账号绑定微信；


# 5.16
HGPlaybackRateView
        [self.player.defaultEdgeControlLayer.topAdapter addItem:subtitleItem];
        [self.player.defaultEdgeControlLayer.topAdapter reload];        
# 5.15

NSArray *fontFamilies = [UIFont familyNames];
for (int i = 0; i < [fontFamilies count]; i++)
{
    NSString *fontFamily = [fontFamilies objectAtIndex:i];
    NSArray *fontNames = [UIFont fontNamesForFamilyName:[fontFamilies objectAtIndex:i]];
    NSLog (@"fontFamiliy----->: %@: %@", fontFamily, fontNames);
}

    //  //  PingFangSC-Medium Semibold Semibold  DINAlternate-Bold
    .font([UIFont systemFontOfSize:14.0 weight:UIFontWeightBold])
.foregroundColor([UIColor whiteColor])
.strokeWidth(-4.0)
.strokeColor([UIColor blackColor])
.allRange();
# 5.14
会议秘书

HGChooseRankTypeView

+ (nullable NSDictionary<NSString *, id> *)modelContainerPropertyGenericClass {
    return @{
        @"subTypeList" : HGSoundTypeListModel.class
    };
}

//                    NSArray<HGSoundTypeListModel *> *subList = [JHModelMapper modelArrayWithJsonArray:obj.subTypeList modelClass:[HGSoundTypeListModel class]];
    CGRect onViewFrame = [self.onView convertRect:self.onView.bounds toView:nil];


有个二级分类列表，要有展开勾选的功能：表格如下：
折叠按钮 ： 分类一
勾选 二级分类1
勾选 二级分类2
折叠按钮 ： 分类二
勾选 二级分类二1
勾选 二级分类二2
勾选 （没有折叠按钮）分类三
注意：分类如有没有下级的 直接显示勾选

# 5.13
抖音基础设置；回复设置（特殊私信回复规则设置）
```objc
- (void)setModel:(HGAccountManageListModel *)model{
    _model = model;
    [self.avatarImageView sd_setImageWithURL:[NSURL URLWithString:model.avatar] placeholderImage:[UIImage imageWithColor:[UIColor colorWithHexString:@"EEEEEE"]]];
    self.nameLab.text = (model.remark == nil || model.remark.length == 0)?model.nickname:model.remark;
//    self.tagLab.text = model.thirdAccountCategoryName;
    self.dyNumLb.text = [NSString stringWithFormat:@"抖音号：%@",model.dyId];
  }
```

```objc
BOOL shouldExitLoop = NO;
NSTimeInterval startTime = [NSDate timeIntervalSinceReferenceDate];
while (!shouldExitLoop) {
    [NSThread sleepForTimeInterval:0.1];
    NSTimeInterval currentTime = [NSDate timeIntervalSinceReferenceDate];
    NSTimeInterval elapsedTime = currentTime - startTime;
    if (elapsedTime >= 2.0) {
        shouldExitLoop = YES;
    }
}
```

# 5.11
抖音拓客（抖音基础设置） 接口
- (instancetype)init {
    self = [super init];
    if (self) {
        _customerType = @"3,5";
    }
    return self;
}


# 5.10
榜单UI 0.5
字幕UI bug修复
44
55

44
50


# 5.8
字幕子线程处理、降噪点击字幕丢失处理
feat 横竖屏视频切换全屏 区分字幕

FormInputTagsCollectTableCell
删除标签

```objc
unSelectIcon

    self.selectionStyle = UITableViewCellSelectionStyleNone;
HGAddWxChooseTableCell * cell = [tableView dequeueReusableCellWithIdentifier:@"HGAddWxChooseTableCell" forIndexPath:indexPath];
    cell.checkBoxBlock = ^(BOOL selected) {
        if (selected) {
            // 如果未选中，则添加该行的索引
            [self.selectedRows addObject:indexPath];
        } else {
            // 如果已选中，则移除该行的索引
            [self.selectedRows removeObject:indexPath];
        }
    };

    // 判断该行是否被选中
    if ([self.selectedRows containsObject:indexPath]) {
        cell.isCheckBtnSelected = YES;
    } else {
        cell.isCheckBtnSelected = NO;
    }
    return cell;
```
# 5.6
- UI 抖音设置
sourceTree报错：Updates were rejected because the tag already exists in the remote.
解决办法是：在当前项目文件夹下
1，执行命令 获取所有的标签
git pull --tags
2、执行命令 覆盖本地存在的标签冲突
git pull --tags -f
再次pull-push就可以了

# 4.30
人才猎手 多选地址

【增加多选地址功能】
https://www.tapd.cn/37438467/prong/stories/view/1137438467001008398

小学生需要做一个身边的科学的科普演讲，聚焦某个事物或者现象，进行科普：
遵循提出问题 做出预测 制定计划 收集证据 分析证据 得出结论 总结反思的过程，
给我出一个关于特斯拉汽车自动驾驶的文案,要利于小学生去演讲、和理解。

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
 0 1 互斥
0
1
2

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
利用FFmpeg库，实现了音频文件音量的增益、降噪；视频文件的格式转化；截取视频指定时间段、视频拼接

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
