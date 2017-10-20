# *ghost-app-font-weaver* 第0版

> &#8195;&#8195;这是一个ghost博客的插件，能让你的文章使用指定的中文字体！而且是精简过的！目前呢，不同的情况生成的字体大小差别很大，跟文章的字数，文章中不重复的字的个数，源字体，生成字体的格式都有很大的关系，以后还有很大优化的空间。
  
使用方法：
    今天礼拜五，不想写，不过可以考虑请我喝罐可乐，然后私聊。
  


说下目前很严重的几个问题  

      1. 还没有做缓存，每次访问页面都会重新生成字体，虽然生成的很快，但是访问量大了还是有点吃不消（你那个鸟网站有没有人去，你特么没点逼数吗？），以后就做个缓存，每次修改文章的时候生成字体就好了，模板的部分就只管插入css。  
      2. 因为字体是CSS定义的，所以是异步加载而且检测起来很麻烦，再所以字体没加载完的时候会用默认字体，然后在完成的瞬间变成新字体，下一步要改用JS方式加载字体，好知道加载的进度到底怎么样，加载完了再显示文字；或者干脆把字体生成BASE64，写在CSS里，以文本方式同步加载，也不错~  
      3. 现在是全局的字体。Ghost每篇文章都是有自己的meta信息的，以后可以定义让每个文章选择自己的字体。  
      4. 用的字体处理是FontMin，对OTF的支持不是很好，必须先转换成TTF，而且有些TTF也不支持，生成的字会错位，使用之前你得测试一下。
      5. 现在就只生成了TTF，没写其他字体，朋友们只能将就用了，或者自强一点，去改改。   
      6. 最近的天气实在是太冷了，被也变得相当的重，至少有五十斤，不然不会起不来床，寒冷的南方，想念温暖的大兴安岭。  
      7. 虽说没多少东西，但是更新完全看心情，有啥想法留个言，我会看到的。