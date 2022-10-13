# think-captcha
thinkphp5 验证码类库

说三遍：
拷贝v1.0.8，把Session改为了Cache，与原版只能选择一个
拷贝v1.0.8，把Session改为了Cache，与原版只能选择一个
拷贝v1.0.8，把Session改为了Cache，与原版只能选择一个

## 安装
> composer require wen-gg/think-captcha


##使用

###模板里输出验证码

~~~
<div>{:captcha_img()}</div>
~~~
或者
~~~
<div><img src="{:captcha_src()}" alt="captcha" /></div>
~~~
> 上面两种的最终效果是一样的

### 控制器里验证
使用TP5的内置验证功能即可
~~~
$this->validate($data,[
    'captcha|验证码'=>'require|captcha'
]);
~~~
或者手动验证
~~~
if(!captcha_check($captcha)){
 //验证失败
};
~~~