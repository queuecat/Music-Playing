# 效果样式
![在这里插入图片描述](https://img-blog.csdnimg.cn/20201210143347224.gif#pic_center)
# 介绍
仿照网易云音乐的音乐播放组件，使用JavaScript动态生成内容，无需更改原有HTML结构，只需要导入js与css文件即可在页面中拥有与网易云音乐同款的音乐播放组件

[GitHub地址](https://github.com/queuecat/Music-Playing)
[演示页面](http://queuecat.top/demos/音乐播放器/)

# 使用
1.导入music.js和music.css文件
~~~javascript
<script src="./music.js"></script>
<link rel="stylesheet" href="music.css">
~~~
2.music.js中默认提供了三首本地歌曲与三张默认封面，歌曲与位于文件目录中的images与Localmusic文件夹中

3.提供了三个用于插入与删除歌曲的方法
~~~javascript
//添加单个歌曲
pushMusic();//接收一个对象作为参数，其中对象的musicName属性用于指定歌曲地址，musicCover属性用于指定歌曲的封面地址
pushMusic({
"musicName":"./test.mp3",
"musicCover":"./test.jpg"
});

//添加多个歌曲
pushMusicList(objArr);//接收一个对象数组作为参数，其中对象的musicName属性用于指定歌曲地址，musicCover属性用于指定歌曲
pushMusicList([{
"musicName":"./test1.mp3",
"musicCover":"./test1.jpg"
},{
"musicName":"./test2.mp3",
"musicCover":"./test2.jpg"
}]);

//删除原有所有歌曲
clearMusicList();//该方法将会清除已添加的所有歌曲，需要添加歌曲后才能播放
~~~