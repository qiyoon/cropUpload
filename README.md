# cropUpload
图片上传以及裁切上传功能，基于angularjs以及js原生代码裁切功能
##安装或引用
```
<script src="//cdn.bootcss.com/angular.js/1.4.9/angular.js"></script>
<script src="js/image.crop.js"></script>
```
##如何使用
* html标签规则
```
<div  ajax-upload                     
    style="border:solid 5px #333"    
    action="upload.php" 
    preview="preview" 
    jcrop="zuobiao" >上传图片</div>
```    
* 预览-指定id
```
<div id="preview"></div>
```
##参数说明   
#####使用css样式自定义
>
1）action  
——服务端上传地址  
2）preview    
——上传预览或裁切选区，指定ID   
3）jcrop="name"  
——返回裁切结果数据，包含有x1:左边距，x2:右边距，y1:上边距，y2:上边距，height:裁切高，width:裁切宽  
4）name = "file"  
——上传表单的名称
5）accept = "images,application,text"  
——允许的上传类型    
6）thumb = "100,100"  
——预览选区大小，默认100,100  
7）crop = "50,50"  
——初始化或默认裁切大小  
8）auto = true  
——是否自动上传（true || false）  默认自动上传  
9）btn  
——上传按钮 指定ID，如果设置此参数则auto失效  
10）htmls  
——控件选区里可写入Html代码。默认文字：上传图片  
10）scale  
——参数为scale="true"，表示等比缩放；否则自由缩放  

####回调函数返回值
```
var ngUpload = {
    uploading:function(res){
        //回调函数-正在上传，res返回百分比数值
    },
    before:function(ctrl){
        //回调函数-上传之前，ctrl可以执行某些操作
    },
    success:function(file){
        //回调函数-上传成功，返回文件内容等
    }
}
```

##特别说明

##持续更新中……

