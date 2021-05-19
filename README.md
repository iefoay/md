# 数据库文档

<a name="返回顶部"></a>

## 数据表列表

* [ant_server_node_resources()](#ant_server_node_resources_pointer)

* [dm_account_position()](#dm_account_position_pointer)

* [dm_account_tag()](#dm_account_tag_pointer)

* [dm_img_info(图片数据挖掘结果表)](#dm_img_info_pointer)

* [dm_video_info(视频数据挖掘结果表)](#dm_video_info_pointer)

* [download_image()](#download_image_pointer)

* [download_video()](#download_video_pointer)

* [ins_account(用户信息表，动态表，每天更新)](#ins_account_pointer)

* [ins_account_data(用户信息表，动态表，每天更新)](#ins_account_data_pointer)

* [ins_account_rank(Ins账号榜单，热点)](#ins_account_rank_pointer)

* [ins_comment(评论信息表)](#ins_comment_pointer)

* [ins_fans(粉丝表)](#ins_fans_pointer)

* [ins_follow(关注表)](#ins_follow_pointer)

* [ins_media(帖子正文表)](#ins_media_pointer)

* [ins_photo_tag(Lin创建。主要是存储武器的1000个类别和建筑的10000个类别的层次关系)](#ins_photo_tag_pointer)

* [ins_process_category()](#ins_process_category_pointer)

* [ins_tag()](#ins_tag_pointer)

* [ins_tag_rank()](#ins_tag_rank_pointer)

* [ins_tag_rank_zhuangbei()](#ins_tag_rank_zhuangbei_pointer)

* [log_running_erro()](#log_running_erro_pointer)

* [monitor_account(用户监控达人表)](#monitor_account_pointer)

* [monitor_tag(用户监控达人表)](#monitor_tag_pointer)

* [proxy_ips_middle()](#proxy_ips_middle_pointer)

* [receive_content()](#receive_content_pointer)

* [spider_job_account(爬虫博主信息采集日常任务)](#spider_job_account_pointer)

* [spider_job_account_fans(爬虫博主粉丝采集日常任务)](#spider_job_account_fans_pointer)

* [spider_job_account_fans_temp(爬虫博主粉丝采集一次性任务)](#spider_job_account_fans_temp_pointer)

* [spider_job_account_follow(爬虫博主关注采集日常任务)](#spider_job_account_follow_pointer)

* [spider_job_account_follow_temp(爬虫博主信息采集一次性任务)](#spider_job_account_follow_temp_pointer)

* [spider_job_account_media(爬虫博主帖子采集日常任务)](#spider_job_account_media_pointer)

* [spider_job_account_media_temp(爬虫博主帖子采集临时任务)](#spider_job_account_media_temp_pointer)

* [spider_job_account_temp(爬虫博主信息采集一次性任务)](#spider_job_account_temp_pointer)

* [spider_job_assign(爬虫任务分配表，记录从爬虫任务表插入到爬虫任务队列的信息)](#spider_job_assign_pointer)

* [spider_job_comment_temp(爬虫帖子评论采集任务)](#spider_job_comment_temp_pointer)

* [spider_job_fail(爬虫任务识别表)](#spider_job_fail_pointer)

* [spider_job_image_temp(爬虫图片采集临时任务，一个记录一个图片\r\n)](#spider_job_image_temp_pointer)

* [spider_job_name_dict(爬虫任务名称字典)](#spider_job_name_dict_pointer)

* [spider_job_queue_stat(爬虫节点状态监控，小时级更新数据,注意每一批数据，更新的时间点应该一致)](#spider_job_queue_stat_pointer)

* [spider_job_queue_stat_hourly(爬虫节点状态监控，小时级更新数据,注意每一批数据，更新的时间点应该一致)](#spider_job_queue_stat_hourly_pointer)

* [spider_job_tag_media(爬虫标签帖子采集日常任务)](#spider_job_tag_media_pointer)

* [spider_job_tag_media_temp(爬虫标签帖子采集临时任务)](#spider_job_tag_media_temp_pointer)

* [spider_job_url_media(爬虫帖子采集日常任务)](#spider_job_url_media_pointer)

* [spider_job_url_media_temp(爬虫帖子评论采集一次性任务)](#spider_job_url_media_temp_pointer)

* [spider_job_video_temp(爬虫博主帖子采集临时任务)](#spider_job_video_temp_pointer)

* [spider_node_job_stat(爬虫任务信息，天级统计，任务数量合并到一起)](#spider_node_job_stat_pointer)

* [spider_node_stat()](#spider_node_stat_pointer)

* [spider_node_stat_daily()](#spider_node_stat_daily_pointer)

* [spider_node_stat_hourly()](#spider_node_stat_hourly_pointer)

* [spider_resource_account()](#spider_resource_account_pointer)

* [spider_resource_account_proxy()](#spider_resource_account_proxy_pointer)

* [spider_resource_proxy(代理ip表)](#spider_resource_proxy_pointer)

* [user(用户表)](#user_pointer)

* [user_job_account(用户任务表-博主采集任务)](#user_job_account_pointer)

* [user_job_tag(任务表-ins社交博主)](#user_job_tag_pointer)

* [user_job_url(任务表-ins社交博主)](#user_job_url_pointer)

* [user_operate_log(用户操作日志)](#user_operate_log_pointer)

* [user_project(信息表-社交项目管理)](#user_project_pointer)

* [user_token(用户登录token库)](#user_token_pointer)



## 数据表说明

<a name="ant_server_node_resources_pointer"></a>

* ant_server_node_resources表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|md5id|varchar(64)||
|server_ip|varchar(128)|站点ip|
|server_no|char(8)|槽位号|
|server_name|varchar(128)|站点名称|
|server_nic_name|varchar(128)|节点昵称|
|server_desc|varchar(512)|站点描述|
|state|int(1)|onoff 启用停用 0-启用 1-停用|
|ability|varchar(512)|每个能力一条记录 如：01|
|update_time|datetime|更新时间|
|tagid|char(2)||
|input_user|varchar(32)|录入人|
|input_time|datetime|录入时间 时间戳 如：yyyyMMddHHmmss:SSS|
|user_org|varchar(64)||
|remarks|varchar(128)||
|reserved1|varchar(128)||
|reserved2|varchar(128)||
|reserved3|varchar(128)||

<a name="dm_account_position_pointer"></a>

* dm_account_position表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account_id|varchar(200)||
|account_name|varchar(200)||
|country|varchar(200)|国家|
|city|varchar(200)|城市|
|update_time|datetime||

<a name="dm_account_tag_pointer"></a>

* dm_account_tag表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account_id|varchar(200)||
|account_name|varchar(200)||
|tag|varchar(1024)|达人标签列表|
|update_time|datetime||

<a name="dm_img_info_pointer"></a>

* dm_img_info表(图片数据挖掘结果表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|img_id|varchar(200)|图片id|
|img_url|varchar(200)|图片url|
|tag|varchar(200)|图片标签，逗号分割|
|fetch_time|datetime|获取时间|

<a name="dm_video_info_pointer"></a>

* dm_video_info表(视频数据挖掘结果表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|video_id|varchar(200)|视频id|
|video_url|varchar(200)|视频图片url|
|tag|varchar(200)|图片标签，逗号分割|
|baidu_source|varchar(200)|百度的视频存储地址|
|baidu_media|text|基础处理信息，包括关键词等|
|baidu_object_detect|text|百度的物体识别信息|
|baidu_character|text|百度文本识别|
|baidu_speech|text|百度语音识别内容|
|fetch_time|datetime|获取时间|
|dm_is_process|int(2)|是否获取数据结果0：没有，1：已经同步|

<a name="download_image_pointer"></a>

* download_image表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|img_url|text|图片地址|
|img_url_local|varchar(100)|图片下载后本地存储的名字|
|img_type|int(2)|图片类型  1：头像图片  2：帖子封面图  3：帖子中的图片|
|is_push_redis|int(2)|是否已经推送到redis下载队列  0：未推送  1：已推送|
|is_download|int(2)|是否已经下载  0：未下载  1：已下载|
|fetch_day|date|存入数据表的日期|
|fetch_time|datetime|存入数据表的日期时间|
|download_time|datetime|下载的时间|
|is_push_oss|int(2)|是否推送至oss|
|push_redis_time|datetime|推送到redis的时间|

<a name="download_video_pointer"></a>

* download_video表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|video_url|text|视频地址|
|video_url_local|varchar(100)|视频下载后本地存储的名字|
|is_push_redis|int(2)|是否已经推送到redis下载队列  0：未推送  1：已推送|
|is_download|int(2)|是否已经下载  0：未下载  1：已下载|
|fetch_day|date|存入数据表的日期|
|fetch_time|datetime|存入数据表的日期时间|
|download_time|datetime|下载的时间|
|is_push_oss|int(2)|是否已经推送到oss|
|push_redis_time|datetime||

<a name="ins_account_pointer"></a>

* ins_account表(用户信息表，动态表，每天更新)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(10)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime|爬虫分配任务时间|
|account_id|varchar(32)|账号id|
|account_name|varchar(64)|用户名|
|account_nick|varchar(512)|全名|
|email|varchar(255)|用户邮箱|
|biography|text|简介|
|external_url|varchar(512)|外部链接|
|profile_pic_url|varchar(512)|头像url|
|profile_pic_url_local|varchar(512)|头像_本地下载本地后的地址|
|media_count|int(10)|发帖数|
|fans_count|int(10)|粉丝数|
|follow_count|int(10)|关注数|
|is_verified|tinyint(3)|是否认证账号 1：认证，0：非认证|
|is_private|tinyint(3)|用户类型 是否私有 1：个人账号 0：公众（任何人都可以看到）|
|country|varchar(64)|地理位置信息|
|city|varchar(255)||
|address|varchar(255)||
|longitude|varchar(100)|经度|
|latitude|varchar(100)|纬度|
|fetch_day|date|更新日期|
|dm_tag1|varchar(255)|第一类标签，四个类别：军工、智库、军队、政府|
|dm_tag1_probability|double|第一类概率|
|dm_tag2|varchar(255)|第二类标签，自己训练的二十多个标签|
|dm_tag2_probability|double|第二类概率|
|dm_country|varchar(255)|国家区域识别字段|
|dm_city|varchar(255)|城市区域识别字段|
|tag_follow|text|博主关注的话题，多个逗号隔开|
|user_mark_account_tag|varchar(255)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家。多个用英文逗号分隔|
|user_mark_account_city|varchar(255)|用户标记-城市。多个用英文逗号分隔|
|fetch_time|datetime|采集时间|
|update_time|datetime|更新时间|

<a name="ins_account_data_pointer"></a>

* ins_account_data表(用户信息表，动态表，每天更新)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(10)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime||
|account_id|varchar(32)|账号id|
|account_name|varchar(64)|用户名|
|account_nick|varchar(512)|全名|
|email|varchar(255)|用户邮箱|
|biography|text|简介|
|external_url|varchar(512)|外部链接|
|profile_pic_url|varchar(512)|头像url|
|profile_pic_url_local|varchar(512)|头像_本地下载本地后的地址|
|media_count|int(10)|发帖数|
|fans_count|int(10)|粉丝数|
|follow_count|int(10)|关注数|
|is_verified|tinyint(3)|是否认证账号 1：认证，0：非认证|
|is_private|tinyint(3)|用户类型 是否私有 1：个人账号 0：公众（任何人都可以看到）|
|country|varchar(64)|地理位置信息|
|city|varchar(255)||
|address|varchar(255)||
|longitude|varchar(100)|经度|
|latitude|varchar(100)|纬度|
|fetch_day|date|更新日期|
|fetch_time|datetime|采集时间|
|update_time|datetime|更新时间|
|dm_tag1|varchar(255)|第一类标签，四个类别：军工、智库、军队、政府|
|dm_tag1_probability|double|第一类概率|
|dm_tag2|varchar(255)|第二类标签，自己训练的二十多个标签|
|dm_tag2_probability|double|第二类概率|
|dm_country|varchar(255)|国家区域识别字段|
|dm_city|varchar(255)|城市区域识别字段|
|tag_follow|text|博主关注的话题，多个逗号隔开|
|user_mark_account_tag|varchar(255)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家|
|user_mark_account_city|varchar(255)|用户标记-城市|

<a name="ins_account_rank_pointer"></a>

* ins_account_rank表(Ins账号榜单，热点)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account_id|varchar(200)|用户id|
|account_name|varchar(200)|用户名，昵称|
|account_nick|varchar(200)|用户昵称|
|fans_count|int(11)|粉丝数|
|country|varchar(200)|国家|
|profile_pic_url|varchar(512)|头像|
|rank|int(11)|排名|
|source|varchar(200)|媒体来源|
|category_tag|varchar(200)|类别|
|category_id|varchar(200)|类别id|
|fetch_time|datetime|获取时间|
|biography|varchar(2550)|自我简介|
|profile_pic_url_local|varchar(512)|头像地址本地|
|fetch_day|date|采集日期|

<a name="ins_comment_pointer"></a>

* ins_comment表(评论信息表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime||
|account_id|varchar(32)|账号id|
|media_id|varchar(32)|帖子id|
|comment_id|varchar(32)|评论id|
|comment_parent_id|varchar(32)|评论父id|
|comment_account_id|varchar(32)|评论账号id|
|comment_account_name|varchar(255)|评论账号名|
|profile_pic_url|varchar(512)|头像url|
|profile_pic_url_local|varchar(255)||
|text|text|评论内容|
|mentioned_tags|varchar(1024)|评论提及标签词#..#..json|
|mentioned_accounts|varchar(512)|评论提及人@..@..json|
|fetch_day|date|抓取日期|
|fetch_time|datetime|抓取时间|
|create_time|datetime|评论创建的日期|
|update_time|datetime|评论更新时间|
|comment_is_dm_sentiment|int(1)||
|dm_comment_sentiment|varchar(255)|情感分析标签|

<a name="ins_fans_pointer"></a>

* ins_fans表(粉丝表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime||
|account_id|varchar(50)|当前主账号|
|account_name|varchar(50)|账号名称|
|account_nick|varchar(50)|账号全名|
|fans_account_id|varchar(50)|粉丝账号id|
|fans_account_name|varchar(255)|粉丝账号名称|
|fans_account_nick|varchar(255)|粉丝账号全名|
|profile_pic_url|varchar(1024)|头像url|
|profile_pic_url_local|varchar(255)|头像url本地|
|is_follow|tinyint(1)|关注关系存续状态，1-存在关注关系，0-取消关注|
|fetch_day|date|采集日期|
|fetch_time|datetime|采集时间|
|update_time|datetime|更新时间|

<a name="ins_follow_pointer"></a>

* ins_follow表(关注表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime||
|account_id|varchar(50)|当前主账号|
|account_name|varchar(255)|博主名|
|account_nick|varchar(255)|博主全名|
|follow_account_id|varchar(50)|被关注账号id|
|follow_account_name|varchar(50)|被关注账号名称|
|follow_account_nick|varchar(50)|被关注账号全名|
|profile_pic_url|varchar(1024)|头像url|
|profile_pic_url_local|varchar(255)|头像url本地|
|is_follow|tinyint(1)|关注关系存续状态，1-存在关注关系，0-取消关注|
|fetch_day|date|采集日期|
|fetch_time|datetime|采集时间|
|update_time|datetime|更新时间|

<a name="ins_media_pointer"></a>

* ins_media表(帖子正文表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime|爬虫工作时间|
|account_id|varchar(32)|发帖账号id|
|account_name|varchar(64)|用户名|
|account_nick|varchar(512)|全名|
|profile_pic_url|varchar(512)|头像url|
|profile_pic_url_local|varchar(255)|头像url（本地）|
|media_id|varchar(32)|帖子id|
|media_url|varchar(512)|帖子url|
|media_cover_url|varchar(512)|帖子封面图地址|
|media_cover_url_local|varchar(255)|帖子封面图地址（本地）|
|title|text|标题|
|text|text|正文|
|like_count|int(10)|点赞数|
|comment_count|int(10)|评论数|
|is_video|tinyint(3)|是否是视频，1：视频 0：图片|
|country|varchar(255)||
|city|varchar(128)|地理位置信息|
|address|varchar(255)||
|longitude|float|经度|
|latitude|float|纬度|
|tag|varchar(128)|帖子所属话题标签|
|video_view_count|int(10)|视频播放数|
|mentioned_accounts|text|帖子提及人|
|mentioned_tags|text|帖子提及标签|
|media_tag_category|text|附件媒体分类标签，算法。多个用竖线分割|
|taken_at|int(20)|发帖时间戳|
|create_time|datetime|发帖时间|
|fetch_day|date|采集时间|
|fetch_time|datetime|采集时间|
|update_time|datetime|更新时间|
|crawl_ip|varchar(255)|采集服务器IP|
|carousel_media_url|text|附件媒体URL\r\n	文章含有媒介时，多个之间用’|’隔开。比如：www.sina.com/1.png | www.baidu.cn/2.doc\r\n	media_url 与 media_type 一一对应\r\n|
|carousel_media_type|varchar(128)|媒介类型\r\n‘P’:  图片；\r\n‘M’:  音频；\r\n‘V’:  视频；\r\n‘X’:  附件(文章)\r\n	文章含有媒介时，多个之间用’|’隔开。比如：P|P|V|X\r\n	media_type 与 media_url 一一对应\r\n|
|carousel_media_url_name|text|附件媒体URL本地。文章含有媒介系统生成文件名，用于下载文件后关联及内容模型识别结果回更，多个文件名之间用’|’隔开。比如\r\n	发帖图片\\视频、附件文件名的组成：账号id+ “_”+发文id+ “_”+引用/转发/分析互动id+ext\r\n1614294429__4048927425118605_4048927425118113_.pdf\r\n	账号头像文件名的组成：账号id+ “_”+photo+ “_”+ext\r\n1614294429_photo_.jpg\r\n	账号banner文件名的组成：账号id+ “_”+banner+ “_”+ext\r\n1614294429_banner_.jpg\r\n|
|carousel_media_title|text|附件媒体文字\r\n	文章含有媒介时，多个之间用’|’隔开。比如：图片1|图片2|附件1\r\n	media_title与 media_type 一一对应\r\n|
|download_status|int(3)|是否已下载。|
|carousel_data|text|包含的媒体信息：如头像、帖子图片、帖子视频，帖子封面|
|img_url|text|多个图片，竖线隔开|
|video_url|text,||
|img_url_local|text,||
|video_url_local|text,||
|dm_cover_image_tag|varchar(255)|识别图片标签 tag_name,tag_pro|tag_name,tag_pro|
|dm_cover_image_google_tag|varchar(255)|google识图识别|
|dm_cover_image_baidu_tag|varchar(255)|baidu识图识别|
|dm_text_tag|varchar(255)|正文关键词提取标签|
|dm_text_sentiment|varchar(255)|情感分析标签:1为正向，2为负向，3为中立|

<a name="ins_photo_tag_pointer"></a>

* ins_photo_tag表(Lin创建。主要是存储武器的1000个类别和建筑的10000个类别的层次关系)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|origin_tag|varchar(255)|原始标签名|
|processed_tag|varchar(255)|处理后的标签名|
|father_tag|varchar(255)|父标签的name|
|level|varchar(255)|所属层次|
|category|varchar(255)|weapons或者architectures|

<a name="ins_process_category_pointer"></a>

* ins_process_category表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|category_id|varchar(200)||
|category_name|varchar(255)||

<a name="ins_tag_pointer"></a>

* ins_tag表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(32)||
|user_job_id|varchar(1024)|用户任务id|
|spider_job_id|varchar(1024)|爬虫任务id|
|spider_job_time|datetime|爬虫任务分配时间|
|tag|varchar(255)||
|tag_id|varchar(32)||
|is_allow_following|int(4)|是否允许关注：\r\n0：不可关注\r\n1：可以关注|
|fetch_day|date||
|fetch_time|datetime||
|media_count|int(20)|话题下帖子的数量|
|update_time|datetime||

<a name="ins_tag_rank_pointer"></a>

* ins_tag_rank表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|tag_id|varchar(200)||
|name|varchar(255)|标签内容|
|media_count|int(11)||
|formatted_media_count|varchar(200)||
|search_result_subtitle|varchar(200)||
|profile_pic_url|varchar(200)||
|use_default_avatar|int(11)||
|fetch_time|datetime||

<a name="ins_tag_rank_zhuangbei_pointer"></a>

* ins_tag_rank_zhuangbei表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|tag|varchar(255)||
|source|varchar(255)||

<a name="log_running_erro_pointer"></a>

* log_running_erro表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|host_ip|varchar(32)|主机ip|
|api_url|varchar(255)|请求接口api|
|api_resp_con|varchar(255)|请求返回值|
|start_time|datetime|请求时间|
|status|int(1)|重采状态 0- 否 1-是|
|queue|varchar(32)|队列编号|
|fail_count|int(4)|失败次数|
|audit_log|text|备注|
|server_no|varchar(20)|槽位号|

<a name="monitor_account_pointer"></a>

* monitor_account表(用户监控达人表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|phone|varchar(100)|用户唯一id, 手机号 |
|account_id|varchar(100)|达人id|
|hour|int(11)|监控小时数，-1为永久任务|
|status|tinyint(1)|监控状态: 0 已删除, 1 监控中|
|create_time|timestamp|创建时间|
|update_time|timestamp|更新时间|

<a name="monitor_tag_pointer"></a>

* monitor_tag表(用户监控达人表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|phone|varchar(100)|用户唯一id, 手机号 |
|tag|varchar(100)|需要监控的标签|
|hour|int(11)|监控小时数，-1为永久任务|
|status|tinyint(1)|监控状态: 0 已删除, 1 监控中|
|create_time|timestamp|创建时间|
|update_time|timestamp|更新时间|

<a name="proxy_ips_middle_pointer"></a>

* proxy_ips_middle表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account_num_id|int(4)|账号编号|
|proxy_id|int(4)|ip地址|
|init_state|int(4)|初始化状态0- 未初始化 1-初始化|
|cstate|int(4)|0-未占用 1-占用 2-释放|
|state|int(4)|启用停用 0-启用 1-停用|

<a name="receive_content_pointer"></a>

* receive_content表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|content|longtext,||
|type|int(4)|数据类型 \r\n1：标签人气帖子列表\r\n2：标签搜索结果\r\n3：标签信息\r\n4：标签最新贴纸列表\r\n5：粉丝列表\r\n6：关注列表\r\n7：帖子列表\r\n8：用户帖子\r\n9：用户信息|
|is_parse|int(4)|是否已经解析入库0：未解析  1：已解析|
|fetch_day|varchar(20)||
|fetch_time|varchar(20)||

<a name="spider_job_account_pointer"></a>

* spider_job_account表(爬虫博主信息采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID,多个用英文逗号分隔|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id|
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)|1停用，0启用|
|spider_job_time|datetime|任务分配时间|
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|account_id|varchar(32)|博主id|
|account_name|varchar(200)||
|frequency|int(11)|采集频率分钟|
|account_fans_lower_limit|int(11)|粉丝数下限值。重复任务取频率最高更新，默认值=0|
|account_is_dm_tag|int(2)|是否进行博主标签识别，0-不进行，1-进行|
|user_mark_account_tag|varchar(512)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家。多个用英文逗号分隔|
|user_mark_account_city|varchar(255)|用户标记-城市。多个用英文逗号分隔|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="spider_job_account_fans_pointer"></a>

* spider_job_account_fans表(爬虫博主粉丝采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)|爬取任务组id |
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)||
|spider_job_time|datetime||
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)|博主名|
|frequency|int(11)|粉丝采集频率|
|page_num|int(11)|粉丝采集页数|
|fans_collect_deep|int(2)|博主粉丝采集深度。默认1度，最多2度|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="spider_job_account_fans_temp_pointer"></a>

* spider_job_account_fans_temp表(爬虫博主粉丝采集一次性任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)||
|page_num|int(11)||
|fans_collect_deep|int(2)|博主粉丝采集深度。默认1度，最多2度|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_account_follow_pointer"></a>

* spider_job_account_follow表(爬虫博主关注采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)||
|spider_job_time|datetime|爬虫分配任务时间|
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)||
|page_num|int(11)||
|frequency|int(11)||
|follow_collect_deep|int(2)|博主关注采集深度。默认1度，最多2度|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_account_follow_temp_pointer"></a>

* spider_job_account_follow_temp表(爬虫博主信息采集一次性任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)||
|page_num|int(11)||
|follow_collect_deep|int(2)|博主关注采集深度。默认1度，最多2度|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_account_media_pointer"></a>

* spider_job_account_media表(爬虫博主帖子采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)|0：未停止，1：已经止|
|spider_job_time|datetime|爬虫分配任务时间|
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|account_id|varchar(200)|博主ID|
|account_name|varchar(200)|博主名称|
|frequency|int(11)|采集帖子频率|
|page_num|int(11)|采集帖子页数|
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|media_is_dm_tag|int(2)|是否进行用户标签下载，0-不下载 1-下载|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_account_media_temp_pointer"></a>

* spider_job_account_media_temp表(爬虫博主帖子采集临时任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)||
|page_num|int(11)||
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|media_is_dm_tag|int(2)|是否进行用户标签下载，0-不下载 1-下载|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_account_temp_pointer"></a>

* spider_job_account_temp表(爬虫博主信息采集一次性任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)|爬取任务组id |
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|account_id|varchar(32)|博主ID|
|account_name|varchar(200)|博主名|
|account_fans_lower_limit|int(11)|粉丝数下限值。重复任务取频率最高更新，默认值=0|
|account_is_dm_tag|int(2)|是否进行博主标签识别，0-不进行，1-进行|
|user_mark_account_tag|varchar(512)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家。多个用英文逗号分隔|
|user_mark_account_city|varchar(255)|用户标记-城市。多个用英文逗号分隔|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="spider_job_assign_pointer"></a>

* spider_job_assign表(爬虫任务分配表，记录从爬虫任务表插入到爬虫任务队列的信息)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_job_id|varchar(200)|爬虫任务id，抽1个|
|spider_job_group_id|varchar(200)|爬虫分组iid|
|user_job_type|int(11)|用户任务类型，1：日常日任务，2：一次性任务|
|spider_job_name|varchar(300)|爬虫任务名称|
|spider_job_time|datetime|爬虫任务开始时间|
|spider_job_assign_num|int(11)|分配的任务数量|

<a name="spider_job_comment_temp_pointer"></a>

* spider_job_comment_temp表(爬虫帖子评论采集任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|account_id|varchar(200)|博主id|
|media_id|varchar(200)|帖子id|
|comment_page_num|int(11)||
|comment_collect_day_num|int(11)|评论采集天数|
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)||
|spider_job_time|datetime|爬虫分配任务时间|
|create_time|datetime|创建时间|
|source|varchar(255)|用户任务来源|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|

<a name="spider_job_fail_pointer"></a>

* spider_job_fail表(爬虫任务识别表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_job_id|varchar(200)|爬虫任务id|
|spider_job_data|varchar(200)|需要爬取的资源id|
|spider_job_time|timestamp||
|spider_job_queue|varchar(200)||
|create_time|datetime|时间|

<a name="spider_job_image_temp_pointer"></a>

* spider_job_image_temp表(爬虫图片采集临时任务，一个记录一个图片\r\n)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|img_url|varchar(1024)|原始图片链接|
|img_url_local|varchar(1023)|本地图片名称，不带oss域名的绝对路径|
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|create_time|datetime|创建时间|
|update_time|datetime||
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|dm_cover_image_tag|varchar(255)|识别图片标签 tag_name,tag_pro|tag_name,tag_pro|
|dm_cover_image_google_tag|varchar(255)|google识图识别|
|dm_cover_image_baidu_tag|varchar(255)|baidu识图识别|
|download_img_type|int(2)|图片类型  1：头像图片  2：帖子封面图  3：帖子中的图片|
|download_is_push_redis|int(2)|是否已经推送到redis下载队列  0：未推送  1：已推送|
|download_is|int(2)|是否已经下载  0：未下载  1：已下载|
|fetch_day|date|存入数据表的日期|
|fetch_time|datetime||
|download_time|datetime|下载完成时间（这张图片下载完成后更新此字段）|
|download_is_push_oss|int(2)|是否推送至oss(图片下载到本地后推送到oss 更新此字段)0：未推送  1：已推送|
|download_push_redis_time|datetime|推送到redis的时间，与is_push_redis字段关联|

<a name="spider_job_name_dict_pointer"></a>

* spider_job_name_dict表(爬虫任务名称字典)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_job_queue|varchar(200)|任务队列|
|spider_job|varchar(200)|任务中文名|

<a name="spider_job_queue_stat_pointer"></a>

* spider_job_queue_stat表(爬虫节点状态监控，小时级更新数据,注意每一批数据，更新的时间点应该一致)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_job_queue|varchar(255)|任务队列名称|
|spider_job|varchar(255)|任务名称|
|stat|int(2)|状态：0-停用，1-启用|
|spider_job_num|int(11)|队列任务量|
|update_time|datetime|更新时间|
|spider_job_max_num|int(11)||

<a name="spider_job_queue_stat_hourly_pointer"></a>

* spider_job_queue_stat_hourly表(爬虫节点状态监控，小时级更新数据,注意每一批数据，更新的时间点应该一致)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_job_queue|varchar(255)|任务队列名称|
|spider_job|varchar(255)|任务名称|
|stat|int(2)|状态：0-停用，1-启用|
|spider_job_num|int(11)|队列任务量|
|update_time|datetime|更新时间|

<a name="spider_job_tag_media_pointer"></a>

* spider_job_tag_media表(爬虫标签帖子采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)||
|spider_job_time|datetime|爬虫分配任务时间|
|collect_end_day|datetime|采集结束日期|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|tag|varchar(512)|标签名|
|frequency|int(11)|帖子爬取评率|
|page_num|int(11)||
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_tag_media_temp_pointer"></a>

* spider_job_tag_media_temp表(爬虫标签帖子采集临时任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|tag|varchar(200)|标签名|
|page_num|int(11)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime||

<a name="spider_job_url_media_pointer"></a>

* spider_job_url_media表(爬虫帖子采集日常任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|text|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)||
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_is_stop|int(11)||
|spider_job_time|datetime|爬虫分配任务时间|
|collect_end_day|datetime|采集结束日期|
|collect_start_time|varchar(64)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(64)|每日采集的时间范围，结束时间点|
|url|varchar(200)|url|
|frequency|int(11)||
|page_num|int(11)||
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(11)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="spider_job_url_media_temp_pointer"></a>

* spider_job_url_media_temp表(爬虫帖子评论采集一次性任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|text|项目ID,多个用英文逗号分隔|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)||
|spider_job_group_id|varchar(1024)||
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|url|varchar(255)|爬取任务id |
|account_id|varchar(32)|博主ID|
|page_num|int(11)||
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论|
|comment_frequency|int(11)|评论采集频率|
|comment_page_num|int(11)|评论采集页数|
|comment_collect_day_num|int(11)|评论采集天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="spider_job_video_temp_pointer"></a>

* spider_job_video_temp表(爬虫博主帖子采集临时任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|user_job_id|varchar(1024)|用户任务ID|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|spider_job_id|varchar(1024)|爬取任务id |
|spider_job_group_id|varchar(1024)||
|video_url|varchar(1024)|原始图片链接|
|video_url_local|varchar(1023)|本地图片名称，不带oss域名的绝对路径|
|spider_job_stat|int(11)|采集状态# 状态 0-未采集 1-采集中 2-采集完成 4-采集失败|
|spider_job_time|datetime|爬虫分配任务时间|
|create_time|datetime|创建时间|
|update_time|datetime||
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|dm_is_process|int(2)|是否提交大数据处理，0：没提交，1：已提交|
|download_is_push_redis|int(2)|是否已经推送到redis下载队列  0：未推送  1：已推送|
|download_is|int(2)|是否已经下载  0：未下载  1：已下载|
|fetch_day|date||
|fetch_time|datetime||
|download_time|datetime|下载完成时间（视频下载完成后更新此字段）|
|download_is_push_oss|int(2)|是否推送至oss(图片下载到本地后推送到oss 更新此字段)0：未推送  1：已推送|
|download_push_redis_time|datetime|推送到redis的时间，与is_push_redis字段关联|

<a name="spider_node_job_stat_pointer"></a>

* spider_node_job_stat表(爬虫任务信息，天级统计，任务数量合并到一起)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_id|varchar(256)||
|spider_job_queue|varchar(255)||
|spider_job|varchar(255)|任务名称|
|fetch_times|int(11)|抓取次数|
|fetch_day|date|抓取日期|
|fetch_date_num|int(11)|抓取数据条数|
|update_time|datetime||

<a name="spider_node_stat_pointer"></a>

* spider_node_stat表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_id|varchar(255)||
|stat|int(2)|状态：0-停用，1-启用|
|ip|varchar(255)|使用的代理ip|
|account|varchar(255)|使用的账号|
|control_model|int(2)|1-人工控制，2-智能控制（默认），3：agent自主控制|
|spider_job_queue|varchar(255)|任务队列名称|
|spider_job|varchar(255)|任务名称|
|spider_heart_time|datetime|发送心跳时间，最新活跃时间|
|spider_job_account|int(11)|博主信息任务爬取量，包括lines和日常|
|spider_job_account_num|int(11)|数据量|
|spider_job_account_fans|int(11)||
|spider_job_account_fans_num|int(11)||
|spider_job_account_follow|int(11)||
|spider_job_account_follow_num|int(11)||
|spider_job_account_media|int(11)||
|spider_job_account_media_num|int(11)||
|spider_job_tag_media|int(11)||
|spider_job_tag_media_num|int(11)||
|spider_job_url_media|int(11)||
|spider_job_url_media_num|int(11)||
|spider_job_comment|int(11)||
|spider_job_comment_num|int(11)||
|create_time|datetime|爬虫创建时间|
|update_time|datetime|从redis同步时间|

<a name="spider_node_stat_daily_pointer"></a>

* spider_node_stat_daily表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_id|varchar(255)||
|stat|int(2)|状态：0-停用，1-启用|
|ip|varchar(255)|使用的代理ip|
|account|varchar(255)|使用的账号|
|control_model|int(2)|1-人工控制，2-智能控制（默认），3：agent自主控制|
|spider_job_queue|varchar(255)|任务队列名称|
|spider_job|varchar(255)|任务名称|
|spider_heart_time|datetime|发送心跳时间，最新活跃时间|
|spider_job_account|int(11)|博主信息任务爬取量，包括lines和日常|
|spider_job_account_num|int(11)|博主信息任务爬取量，包括lines和日常|
|spider_job_account_fans|int(11)||
|spider_job_account_fans_num|int(11)||
|spider_job_account_follow|int(11)||
|spider_job_account_follow_num|int(11)||
|spider_job_account_media|int(11)||
|spider_job_account_media_num|int(11)||
|spider_job_tag_media|int(11)||
|spider_job_tag_media_num|int(11)||
|spider_job_url_media|int(11)||
|spider_job_url_media_num|int(11)||
|spider_job_comment|int(11)||
|spider_job_comment_num|int(11)||
|create_time|datetime|爬虫创建时间|
|update_time|datetime|从redis同步时间|
|fetch_day|date||

<a name="spider_node_stat_hourly_pointer"></a>

* spider_node_stat_hourly表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|spider_id|varchar(255)||
|stat|int(2)|状态：0-停用，1-启用|
|ip|varchar(255)|使用的代理ip|
|account|varchar(255)|使用的账号|
|control_model|int(2)|1-人工控制，2-智能控制（默认），3：agent自主控制|
|spider_job_queue|varchar(255)|任务队列名称|
|spider_job|varchar(255)|任务名称|
|spider_heart_time|datetime|发送心跳时间，最新活跃时间|
|spider_job_account|int(11)|博主信息任务爬取量，包括lines和日常|
|spider_job_account_num|int(11)|博主信息任务爬取量，包括lines和日常|
|spider_job_account_fans|int(11)||
|spider_job_account_fans_num|int(11)||
|spider_job_account_follow|int(11)||
|spider_job_account_follow_num|int(11)||
|spider_job_account_media|int(11)||
|spider_job_account_media_num|int(11)||
|spider_job_tag_media|int(11)||
|spider_job_tag_media_num|int(11)||
|spider_job_url_media|int(11)||
|spider_job_url_media_num|int(11)||
|spider_job_comment|int(11)||
|spider_job_comment_num|int(11)||
|create_time|datetime|爬虫创建时间|
|update_time|datetime|从redis同步时间|

<a name="spider_resource_account_pointer"></a>

* spider_resource_account表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account|varchar(50)|账号，可作为唯一id|
|password|varchar(50)|密码|
|email|varchar(255)|邮箱|
|email_password|varchar(255)|邮箱密码|
|gmail|varchar(255)|谷歌辅助邮箱|
|gmail_password|varchar(255)|密码|
|is_login|int(4)|0：未登录 1：已登录|
|login_time|datetime|登录时间|
|log_in_a_heartbeat|datetime|维持账号登录心跳，如果判断长时间没有登录心跳，则将登录状态重置为未登录|
|logout_time|datetime|退出登录时间|
|cold_stat|int(2)|1:已冷却  0：冷却中|
|cold_duration|int(4)|需要冷却的时长  单位分钟，默认0|
|cold_start_time|datetime|开始冷却的时间|
|cold_end_time|datetime|冷却结束的时间|
|reg_time|datetime|注册时间|
|live_stat|int(2)|1:可用 0:完全被封 2：需要手动登录解封 3：需要发email申诉解封|
|assign_stat|int(11)|0 未分配，1已分配 2 已使用|
|reg_site|varchar(255)|注册地址|
|fetch_time|datetime|添加时间|
|note|varchar(255)|注释|
|level|int(2)|账号等级 1：最高级 2：一般级别  3：小白账号 |
|source|int(2)|来源 1：外采  2：养号  3：员工账号|
|login_type|int(2)|登录方式 1：web登录 2：app登录 3：开放平台登录  4:其它|
|token|varchar(255)|登陆后的授权token|
|device_id|varchar(255)|设备id|
|jsonData|text|登录相关数据|
|proxy_id|varchar(50)|对应代理表的proxy_id|
|retry_num|int(4)|账号重试次数，账号登录或抓取时报错会进入冷却状态，冷却时间10分钟。每冷却一次次字段自增1，累积20次后记录帐号状态被封|

<a name="spider_resource_account_proxy_pointer"></a>

* spider_resource_account_proxy表()[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|account|varchar(50)|账号|
|proxy_id|varchar(50)|对应代理表中的proxy_id|
|fetch_time|datetime|添加时间|
|ip_port|varchar(200)||
|is_used|int(11)||

<a name="spider_resource_proxy_pointer"></a>

* spider_resource_proxy表(代理ip表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|ip|varchar(255)||
|port|varchar(255)||
|site|varchar(255)|ip所在地|
|ip_type|int(2)| 说明：1:自建ip 2:采购的机房固定ip 3:采购的家庭固定ip|
|is_used|int(2)|是否在使用 1：正在使用  0：未使用， >1 使用次数|
|cold_stat|int(2)|1:已冷却  0：未冷却|
|stat|int(2)|ip是否可用  1:可用  0：不可用|
|ip_map|varchar(255)|如果ip是由国内服务器转发的话，此处应填对应的国外代理服务ip,\r\n详见：https://www.tapd.cn/57293674/documents/show/1157293674001000538?file_type=word|
|proxy_map|varchar(255)||
|proxy_id|varchar(50)|ip+prot+fetch_time的MD5值|
|fetch_time|datetime|最新更新时间|
|retry_num|int(2)|代理ip连接错误，重试次数|

<a name="user_pointer"></a>

* user表(用户表)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|username|varchar(200)|账号名|
|password|varchar(200)|账号密码|
|email|varchar(32)|邮箱|
|phone|varchar(100)|手机号|
|nickname|varchar(200)|昵称|
|avatar|varchar(200)|头像|
|gender|int(4)|性别|
|birthday|date|出生日期|
|address|varchar(200)|地址|
|company|varchar(200)|公司|
|signature|varchar(200)|签名|
|introduction|varchar(200)|自我介绍|
|token|text|token|
|expired|int(11)|过期时间戳|
|level|int(11)|用户等级，1 普通用户；5：管理员|
|user_group|varchar(200)|角色|
|status|int(11)|0正常，-1不正常|
|reg_date|date|注册日期|
|reg_at|timestamp|注册时间|
|fetch_time|datetime|更新时间|

<a name="user_job_account_pointer"></a>

* user_job_account表(用户任务表-博主采集任务)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|varchar(255)|项目id|
|user_id|varchar(255)|录入人id|
|user_job_id|varchar(512)|用户任务id|
|user_job_group_id|varchar(512)|用户任务分组id|
|user_job_type|int(11)|用户任务类型，1：日常日任务，2：一次性任务|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|user_job_is_stop|int(1)|启用停用 0-启用 1-停用|
|collect_end_day|datetime|采集结束日期，对所有子任务通用|
|collect_start_time|varchar(255)|每日采集的时间范围，开始时间点，对所有子任务通用|
|collect_end_time|varchar(255)|每日采集的时间范围，结束时间点，对所有子任务通用|
|account_id|varchar(255)|博主id|
|account_name|varchar(255)|博主账号名称|
|account_nick|varchar(255)|博主昵称|
|account_is_collect|int(2)|是否采集用户信息 1-是 0-否|
|account_frequency|int(4)|采集用户信息频率，分钟|
|account_fans_lower_limit|int(11)|只对博主。粉丝数下限值。重复任务取频率最高更新，默认值=0|
|account_is_dm_tag|int(2)|是否进行博主标签识别，0-不进行，1-进行|
|user_mark_account_tag|varchar(512)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家|
|user_mark_account_city|varchar(255)|用户标记-城市|
|fans_is_collect|int(2)|是否采集粉丝 1-是 0-否|
|fans_frequency|int(11)|粉丝采集频率|
|fans_page_num|int(4)|粉丝采集页数|
|fans_collect_deep|int(2)|博主粉丝采集深度。默认1度，最多2度|
|follow_is_collect|int(2)|是否采集关注用户 1-是 0-否|
|follow_frequency|int(11)|关注采集频率|
|follow_page_num|int(4)|关注采集页数|
|follow_collect_deep|int(2)|博主关注采集深度。默认1度，最多2度|
|media_is_collect|int(2)|是否采集帖子 1-是 0-否|
|media_frequency|int(11)|博主采集频率。runningValue动态调整值|
|media_page_num|int(4)|需要采集的帖子页数|
|media_like_lower_limit|int(11)|只对帖子。点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|只对帖子。评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论 1-是 0-否|
|comment_frequency|int(4)|采集评论频率。分钟，默认1天|
|comment_page_num|int(4)|评论采集页数|
|comment_collect_day_num|int(2)|评论采集持续天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|用户录入时间|
|update_time|datetime|用户更新时间|
|is_deleted|int(1)|是否删除 1-是 0-否|

<a name="user_job_tag_pointer"></a>

* user_job_tag表(任务表-ins社交博主)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|varchar(255)|项目id|
|user_id|varchar(255)|录入人|
|user_job_id|varchar(512)|用户任务id|
|user_job_group_id|varchar(512)|用户任务分组id|
|user_job_type|int(11)|用户任务类型，1：日常日任务，2：一次性任务|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|user_job_is_stop|int(1)|启用停用 0-启用 1-停用|
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(255)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(255)|每日采集的时间范围，结束时间点|
|tag|varchar(255)|标签名|
|media_is_collect|int(2)|是否采集帖子 1-是 0-否|
|media_frequency|int(4)|采集帖子频率。分钟，默认1天|
|media_page_num|int(4)|需要采集的帖子页数|
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论 1-是 0-否|
|comment_frequency|int(4)|采集评论频率。分钟，默认1天|
|comment_page_num|int(4)|评论翻页数|
|comment_collect_day_num|int(2)|评论采集持续天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|用户录入时间 时间戳 如：yyyyMMddHHmmss:SSS|
|update_time|datetime|用户更新时间|
|is_deleted|int(1)|是否删除 1-是 0-否|

<a name="user_job_url_pointer"></a>

* user_job_url表(任务表-ins社交博主)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|编号|
|project_id|varchar(128)|项目id|
|user_id|varchar(255)|录入人|
|user_job_id|varchar(512)|用户任务id|
|user_job_group_id|varchar(512)|用户任务组id|
|user_job_type|int(11)|用户任务类型，1：日常日任务，2：一次性任务|
|user_job_level|int(2)|任务等级 level1...level6 默认level 3|
|user_job_is_stop|int(1)|启用停用 0-启用 1-停用|
|collect_end_day|datetime|采集结束时间|
|collect_start_time|varchar(255)|每日采集的时间范围，开始时间点|
|collect_end_time|varchar(255)|每日采集的时间范围，结束时间点|
|url|varchar(512)|url|
|tag|varchar(255)|标签名|
|account_id|varchar(255)|博主id|
|account_name|varchar(255)|博主名|
|account_is_collect|int(2)|是否采集用户信息 1-是 0-否|
|account_frequency|int(4)|采集用户信息频率，分钟|
|account_fans_lower_limit|int(11)|粉丝数下限值。重复任务取频率最高更新，默认值=0|
|account_is_dm_tag|int(2)|是否进行博主标签识别，0-不进行，1-进行|
|user_mark_account_tag|varchar(512)|用户标记-标签。多个用英文逗号分隔|
|user_mark_account_country|varchar(255)|用户标签-国家|
|user_mark_account_city|varchar(255)|用户标记-城市|
|fans_is_collect|int(2)|是否采集粉丝 1-是 0-否|
|fans_frequency|int(11)|粉丝采集频率|
|fans_page_num|int(4)|翻页数|
|fans_collect_deep|int(2)|博主粉丝采集深度。默认1度，最多2度|
|follow_is_collect|int(2)|是否采集关注用户 1-是 0-否|
|follow_frequency|int(11)|关注采集频率|
|follow_page_num|int(4)|关注，采集页数|
|follow_collect_deep|int(2)|博主关注采集深度。默认1度，最多2度|
|media_is_collect|int(2)|是否采集帖子 1-是 0-否|
|media_frequency|int(4)|博主采集频率。runningValue动态调整值|
|media_page_num|int(4)|需要采集的帖子页数|
|media_like_lower_limit|int(11)|点赞数下限值。重复任务取频率最高更新，默认值=0|
|media_comment_lower_limit|int(11)|评论数下限值。重复任务取频率最高更新，默认值=0|
|media_is_download_image|int(2)|是否进行用户图片下载，0-不下载 1-下载|
|media_is_download_video|int(2)|是否进行用户视频下载，0-不下载 1-下载|
|media_is_dm_image|int(2)|是否进行图片识别，0-不进行，1-进行|
|media_is_dm_video|int(2)|是否进行视频识别，0-不进行，1-进行|
|media_is_dm_tag|int(2)|是否进行帖子标签识别，0-不进行，1-进行|
|comment_is_collect|int(2)|是否采集评论 1-是 0-否|
|comment_frequency|int(4)|采集评论频率。分钟，默认1天|
|comment_page_num|int(4)|评论翻页数|
|comment_collect_day_num|int(2)|评论采集持续天数|
|comment_is_dm_sentiment|int(2)|是否进行情感分析识别，0-不识别 1-识别|
|create_time|datetime|用户录入时间 时间戳 如：yyyyMMddHHmmss:SSS|
|update_time|datetime|用户更新时间|
|is_deleted|int(1)|是否删除 1-是 0-否|

<a name="user_operate_log_pointer"></a>

* user_operate_log表(用户操作日志)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)||
|log_id|varchar(100)|日志id|
|user_id|varchar(100)|用户id|
|user_name|varchar(100)|用户名|
|host|varchar(100)|达人id|
|remark|text|备注|
|create_time|datetime|创建时间|
|update_time|datetime|更新时间|

<a name="user_project_pointer"></a>

* user_project表(信息表-社交项目管理)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|int(11)|id|
|creator|varchar(32)|创建人|
|creator_org|varchar(64)|所属机构|
|pm|char(128)|所属项目经理|
|project_id|varchar(255)|项目id|
|project_no|varchar(255)|项目编号/代号-新增任务remark属性以逗号“，”分隔|
|project_name|varchar(255)|项目名称|
|is_priority|char(1)|是否重点项目 0-普通 1-重点重点项目评论不能治理|
|remarks|varchar(512)|备注|
|create_time|datetime|录入时间|
|update_time|datetime|更新时间|
|is_deleted|int(1)|是否已删除 1-是 0-否|

<a name="user_token_pointer"></a>

* user_token表(用户登录token库)[↑](#返回顶部)

|字段名称|字段类型|字段含义|
|:---:|:---:|:---:|
|id|bigint(20)||
|user_id|int(10)|用户ID|
|account|varchar(256)|账号名|
|token|varchar(256)|token|
|ip|varchar(256)|用户ip|
|session_id|varchar(100)|场景id|
|login_time|datetime|用户登录时间|
|action_time|datetime|用户最后活动时间|

