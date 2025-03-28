# 今日校园请假系统使用手册

## 项目介绍
今日校园请假系统是一个专门为在校学生设计的请假管理平台。本系统支持学生在线提交请假申请、查看审批进度、进行请假核验等功能，极大地简化了传统请假流程，提高了请假效率。

## 部署说明

### 环境要求
1. Web服务器：Apache/Nginx
2. 操作系统：Windows/Linux
3. 浏览器支持：Chrome、Firefox、Safari等现代浏览器

### 部署步骤
1. 下载项目文件
   - 将项目所有文件下载到本地

2. 配置Web服务器
   - Apache配置：
     1. 将项目文件放置在Apache的根目录（如：htdocs）
     2. 确保.htaccess文件存在并配置正确
   
   - Nginx配置：
     1. 将项目文件放置在Nginx的网站目录
     2. 配置nginx.conf，添加如下配置：
     ```nginx
     server {
         listen 80;
         server_name your_domain.com;
         root /path/to/your/project;
         index index.html;
         
         location / {
             try_files $uri $uri/ /index.html;
         }
     }
     ```

3. 域名设置
   - 购买域名并完成备案（如果在中国大陆部署）
   - 将域名解析到服务器IP
   - 配置SSL证书（推荐使用HTTPS）

4. 访问测试
   - 通过浏览器访问域名
   - 检查各项功能是否正常
   - 测试移动端适配情况

### 注意事项
1. 确保服务器安全
   - 开启防火墙
   - 定期更新系统
   - 设置强密码
2. 定期备份
   - 备份网站文件
   - 备份配置文件
3. 性能优化
   - 开启Gzip压缩
   - 配置浏览器缓存
   - 优化图片资源

## 系统功能使用说明

### 1. 请假申请功能
1. 进入首页，点击"请假申请"按钮
2. 选择请假类型（事假/病假/其他）
3. 填写请假信息：
   - 请假时间（起始时间和结束时间）
   - 请假原因（至少20字详细说明）
   - 上传相关证明材料（如病假需要医院证明）
4. 提交申请后等待审批
5. 可在"我的请假"中查看申请状态

### 2. 请假状态查询
1. 点击首页"我的请假"
2. 可查看所有请假记录：
   - 待审批（黄色标识）
   - 已通过（绿色标识）
   - 已驳回（红色标识）
3. 点击具体请假记录可查看：
   - 详细请假信息
   - 审批流程
   - 审批意见

### 3. 二维码核验使用
1. 进入已批准的请假详情页
2. 点击"生成核验码"按钮
3. 向相关老师出示二维码
4. 二维码包含信息：
   - 学生基本信息
   - 请假时间段
   - 请假类型
   - 审批状态
   注意：二维码每6小时更新一次，请及时更新

### 4. 销假操作指南
1. 请假期满后，点击"销假"按钮
2. 填写销假说明
3. 上传相关材料（如果需要）
4. 等待销假审批

### 5. 智能客服使用
1. 点击界面右下角"客服"图标
2. 可选择以下服务：
   - 常见问题自助查询
   - 人工客服咨询（工作日9:00-17:00）
   - 问题反馈提交

## 注意事项

### 请假规则
1. 请假时间规定：
   - 事假：3天以内由辅导员审批
   - 病假：需要医院证明
   - 长期请假：需要院领导审批
2. 提前申请：请至少提前24小时提交申请
3. 特殊情况：紧急请假请联系辅导员

### 使用提醒
1. 请假期间要保持手机通畅
2. 定期查看请假审批状态
3. 请假期满及时销假
4. 如遇特殊情况需要续假，请在原假期结束前提交