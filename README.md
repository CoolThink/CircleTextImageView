&nbsp;&nbsp;&nbsp;&nbsp;在项目中我们经常遇到需要显示圆形头像的需求，一般我们都使用hdodenhof/CircleImageView的这个开源控件实现(简洁，没多余的东西)。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;而在的项目中我经常遇到这样的一个需求:如果用户上传了头像就显示圆形头像，如果没有上传头像就在圆形背景上显示文字。或者是直接在圆形头像上添加文字。因此我就在CircleImageView基础上实现了一个CircleTextImageView的组件。
CircleTextImageView是一个什么样的组件呢，直接上图吧

1.只显示头像
![只显示头像](http://img.blog.csdn.net/20151218120637337)

2.圆形背景文字
![圆形背景文字](http://img.blog.csdn.net/20151218120953090)

3.头像+文字
![头像+文字](http://img.blog.csdn.net/20151218121007675)

分别的使用方法:
1.只显示头像
```
<com.thinkcool.circletextimageview.CircleTextImageView
        xmlns:app="http://schemas.android.com/apk/res-auto"
        android:id="@+id/profile_image"
        android:layout_width="96dp"
        android:layout_height="96dp"
        android:src="@drawable/hugh"
        app:citv_border_width="2dp"
        app:citv_border_color="#FF000000"/>
```
2.圆形背景文字

```
<com.thinkcool.circletextimageview.CircleTextImageView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            app:citv_border_color="@android:color/white"
            app:citv_border_width="2dp"
            android:layout_gravity="center"
            app:citv_text_text="照片"
            app:citv_text_size="32sp"
            app:citv_text_padding="35dp"
            app:citv_text_color="@android:color/white"
            app:citv_fill_color="#50555D"
            />
```
3.头像+文字

```
<com.thinkcool.circletextimageview.CircleTextImageView
            android:layout_width="96dp"
            android:layout_height="96dp"
            app:citv_border_color="@android:color/darker_gray"
            app:citv_border_width="2dp"
            android:layout_gravity="center"
            app:citv_text_text="晴朗"
            app:citv_text_size="32sp"
            app:citv_text_padding="35dp"
            android:src="@drawable/skye"
            app:citv_text_color="#ff99cc00"
            app:citv_fill_color="#50555D"
            />
```
最后在build.gradle中添加组件即可:
```
compile 'com.github.thinkcool:circletextimageview:1.0.20151218'
```
