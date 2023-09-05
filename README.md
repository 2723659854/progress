### php 进度条
#### 项目介绍
php在cli模式下运行，需要显示进度条。可以使用本插件完成。
#### 安装方法
```bash 
composer require xiaosongshu/progress
```
#### 使用方法
创建index.php文件，写入如下内容：
```php 

/** 创建进度条 */
$bar = new ProgressBar();
/** 总长度 */
$bar->createBar(78);
/** 设置颜色：紫色 （非必选 ，默认白色） */
$bar->setColor('purple');
/** 更新进度条 */
for ($i=1;$i<=11;$i++){
    /** 模拟业务耗时 */
    sleep(1);
    /** 进度条步长 */
    $bar->advance(8);
}

```
执行php index.php ,就可以看到进度条了

#### 联系作者
email:2723659854@qq.com