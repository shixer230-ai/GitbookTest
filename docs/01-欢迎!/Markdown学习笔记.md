# markdown细节回顾
* * *
made by ***zkerur***   
from up主 ***青空の霞光***  
*此文档为学习Markdown时所写,仅作学习辅助工具分享, 无权威性
* * *

说明:  
// : 基础用法  
⚠️ : 注意事项

* * *

## 常规操作

我是一段很普通的文本信息，直接打出来就可以  
//末尾2个空格 + enter换行  
换行～～～

//连续换2行-->换段

我是第二段文本信息

//使用一对 2个星号/下划线  
**关于加粗**  
__下划线也可加粗__

//前后各使用1个星号或者1个下滑线  
*这是斜体*

⚠️下划线选一段也行但中文环境可能失效  

eg:_hello_ world

//使用3个星号进行包围  
***想要既有斜体又有加粗的效果***

___三个下滑线也可以___

//使用一对双波浪线  
~~文本删除线~~

⚠️可以套娃使用*_~  
eg:***~~hallo werld~~***

使用分割线:  
在两端文本的中间行使用 >= 3个的*, 不可在后面添加其他内容, 下划线也可
***
就像这样(^-^), 星号之间可以使用空格隔
* * * * *
开ou～
- - -
⚠️使用-号隔开时, 中间必须要有空格

* * *

## 标题操作

# 标题( 1 级) // # + 1个空格

这样也是1级标题 //下一行加入等号 =
=

## 这是2级标题 // ## + 1个空格

这样也是2级标题 //下一行加入减号 -
-

### 这是3级标题 ( 1 ) // ### + 1个空格以此类推

### 这是3级标题 ( 2 )

### 这是3级标题 ( 3 )
⚠️标题上限至高6级

* * *

## **列表**

### **圆点无序列表**
//使用 星号 / 加号 / 减号 + 1个空格
* hello world
* 这是同一 * 列表
+ hello markdown
+ 这是同一 + 列表
- hello phi
- 这是同一 - 列表

⚠️使用相同的符号(星号 / 加号 / 减号), 才会归为同一列表

### **数字有序列表**

#### 基础格式
//使用 数字 + 点 + 1个空格
1. HELLO WORLD
2. HELLO MARKDOWN
3. HELLO PHI

⚠️数字需要按照从小到大的正整数顺序, 混乱的顺序将不会按照原来的乱序显示  
⚠️其中第一项支持自定义正整数大小

#### 嵌套列表
//前面加入4个空格(tab) + * + 1个空格
1. Hello World
    * 这是嵌套2级列表
2. Hello Markdown
    * 这是嵌套2级列表
3. Hello Phi
    * 这是嵌套2级列表

⚠️>=3级列表同样在前一级列表的基础上前面加上4个空格(tab) + * + 1个空格

### 列表勾选
//在 (* )后加入 ([ ] ), [x/X]勾选
* [ ] hello World
* [x] hello Markdown
* [X] hello Phi

* * *

## 代码块

### 写法

#### 写法1
//代码的前面加入4个空格(tab)

    public class Test {
        public static void main(String[] args) {
            System.out.println("hello world");
            System.out.println("hello markdown");
            System.out.println("hello phi");
        }
    }

⚠️代码块上方需要空1行
#### 写法2
//在代码块的开始和结束使用```(连续 >= 3个)
```
public class Test {
    public static void main(String[] args) {
        System.out.println("Hello World");
        System.out.println("Hello Markdown");
        System.out.println("Hello Phi");
    }
}
```
⚠️如果下方的```没有写, 则会将下面的所有内容并入代码块

### 语言显示

#### 整段
//在```后加入语言名称
```java
public class Test {
    public static void main(String[] args) {
        System.out.println("Hello World");
        System.out.println("Hello Markdown");
        System.out.println("Hello maimai");
    }
}
```

```c
#include <stdio.h>

int main()
{
    printf("hello world\n");
    return 0;
}
```

#### 行内
//在(``)之间加入内容  
算术平方根`sqrt()`方法

* * *

## 引用
//使用 > + 空格符号以引用TA人文章内容, 换行原则遵循2个空格 + enter   
//也可使用空一行的形式换行
> 《Phigros》是由南京鸽游网络有限公司（Pigeon Games）
> 开发的一款非商业音乐节奏类游戏，
> 于2019年8月31日正式发行。游戏完全免费，无任何内购物品，
> 运营方式为售卖周边与玩家自愿捐赠，
> 总策划“CN_115”在官方渠道声明游戏“完全免费、用爱发电且永不收费”。
> 可在TapTap和App Store下载。
> 游戏采用无轨谱面设计，包含
> 1. 点击（Tap）
> 2. 长按（Hold）
> 3. 滑动（Flick）
> 4. 拖拽（Drag）
>
> 四种音符类型，
> 搭配动态变化的判定线。收录超过200首电音曲目，涵盖多种风格，
> 并由数十名插画师绘制大量精美游戏插画。设有严判课题模式等玩法。
> 截至2026年3月，在App Store获得约18.2万个评价，平均分4.7（满分5分）；
> 在TapTap约9.9万个评价中平均分9.6（满分10分）。

⚠️引用当中也可嵌套  
⚠️务必遵循(> )的格式, 同时包括再次引用, 换行操作, 列表嵌套和代码块  
⚠️在列表当中也可使用引用  
(^っ˘ω˘ς^)ﾉｼ

* * *

## 超链接

### 写法
#### 写法1
//写入网址域名  
https://github.com
#### 写法2
//在[]后加上(网址)  
这里是[GitHub](https://github.com)主页
#### 写法3
//在[]后添加[占位符], 之后使用[占位符] + : + 网址域名  
[你][a]好[口][b]牙

[a]:https://github.com
[b]:https://github.com

⚠️使用[占位符] + : + 网址域名之前至少空1行  
⚠️第三种写法更适用于一段文本中插入大量链接

### 注脚
注脚[^1]

[^1]:我在底部

* * *

## 插入图片
//! + [] + ()  
这是插入的图片
![图片](https://www.apple.com/v/home/images/macbook-air-m5/a/hero_macbook_air_m5__eb1idggd120y_large_2x.jpg)
⚠️[]中为alt信息, 当图片无法加载时加载alt信息  
⚠️:也可以使用[占位符], 方式同上  
⚠️:图片大小调整需要html代码

* * *

## 表格
//项与项之间使用|分隔  
//表头下使用-以建立表格  

|  AI大模型名称  |    发布时间     |     模型类型      |
|:--------------:|:---------------:|:-----------------:|
|    Deepseek    |  2025年1月10日  | 纯文本大语言模型  |
|    Chatgpt     | 2023年12月20日  |     混合模型      |
|     Gemini     |  2023年12月6日  |     混合模型      |

* 数据来源于网络

⚠️:左对齐时冒号在左边, 右对齐时冒号在右边, 居中左右均有(:)  
**|:-| & |-:| & |:-:|**

* * *

## 数学

### 字母呈现
//美元 + 字母 + 美元 更清楚地呈现字母  

⚠️:单个$仅适用于单行
#### 写法1
$x + 2x = 6$  
解得 $x = 3$
#### 写法2
$$
3x + 2y = 9
$$

### 分数表达
//使用\frac{分子}{分母}  
$\frac{(2x + 5)·6x}{(4x + 8)·(x + 3)}$
### 幂
//底数 + ^ + 指数  
$2^3 = 8$
### 其它
//下标_  
$He_2^4$

//开方\sqrt[次数]{被开方数}  
$\sqrt{4} = 2$

⚠️:如果在数学公式中使用{}, 则需要在前面加上\

(^/ω＼^)ノ
### 特殊符号
$\not=$ 不等于  
$\approx$ 约等于  
$\leq$ 小于等于  
$\geq$ 大于等于  
$\times$ 乘号  
$\div$ 除号  
$\pm$ 正负号  
$\sum$ 求和  
$\prod$ 累乘  
$\coprod$ 累除  
$\overline{}$ 求平均  
$180^\circ$ 度数  
$\pi$ Π  
$\sin \cos \tan$ 三角函数  
$\infty$ 无穷  
$\int$ 定积分  
$\iint$ (i的个数)重积分  
$f\prime(x)$ 求导  
$\lim$ 极限  
$\in \notin \supset \supseteq \bigcap \bigcup$ 集合  
$\log_2{5}$ 对数  
$\alpha \beta \gamma \delta \eta \omega \theta \sigma \mu$ 希腊字母

## THE END

