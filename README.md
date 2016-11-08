# UnderLineLinkTextView
Support some of the key words can be clicked with the underline TextView<br>
```xml
    <declare-styleable name="AutoLinkStyleTextView">
        <attr name="AutoLinkStyleTextView_text_value" format="string|reference"/>//key word with color and underline, and split with ','(en)
        <attr name="AutoLinkStyleTextView_default_color" format="color|reference"/>//word and underline's color
        <attr name="AutoLinkStyleTextView_has_under_line" format="boolean"/>//underline with true and false
    </declare-styleable>
```
<br>
use, for example:<br>
```xml
    <xx.AutoLinkStyleTextView
        android:id="@+id/tv_clause"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="我已核对付款金额，仔细阅读并同意“购买须知”及约克论坛团购“用户条款”"
        android:textSize="16sp"
        app:AutoLinkStyleTextView_text_value="“购买须知”,“用户条款”"
        />
```
```java
    autoLinkStyleTextView.setOnClickCallBack(new AutoLinkStyleTextView.ClickCallBack() {
        @Override
        public void onClick(int position) {
            if (position == 0) {
                Toast.makeText(MainActivity.this, "购买须知", Toast.LENGTH_SHORT).show();
            } else if (position == 1) {
                Toast.makeText(MainActivity.this, "用户条款", Toast.LENGTH_SHORT).show();
            }
        }
     });
```
![](https://github.com/wangshaolei/UnderLineLinkTextView/blob/master/img/1.png)   ![](https://github.com/wangshaolei/UnderLineLinkTextView/blob/master/img/2.png)
