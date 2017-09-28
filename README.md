# 七鱼官网-公共样式
这是七鱼客服[官网](http://qiyukf.com)的公共样式库(持续更新中...);

使用mcss预处理器编写,故命名: q(iyu)mcss_m(ai)ns(i)t(e);

桌面浏览器端和手机端浏览器,两个版本均写入模块中,以文件名区分;
比如:
```js
@extend u-btn;  // 引入桌面端的抽象类
@extend u-btn0; // 引入手机端的抽象类
```

## 工程目录

**目录:**
```dir
mcss            (工程文件夹)
    |_config    (配置文件)
    |_mixins    (方法类)
    |_abstract  (ui类)
        |_unit  (元件)
        |_mod   (复合件)
        |_grid  (布局件)

test     (业务样式)

```

### _config 配置相关
**目录**
```dir
_config
    |__ _config.mcss    配置变量
    |__ _import.mcss    样式输出 
    |__ _reset.mcss     重置样式单
```

**变量建议**

```js
$g_xxx_yyy  // xxx:主要描述;yyy:辅助描述
// examples:
$g_color = #fff;
$g_bgcolor = #fff;
$g_color_logo = #fff;
$g_bgcolor_primary = #fff;
$g_fontsize_normal = #fff;
```


### _mixins 方法类
**目录:**
```dir
_mixins
    |__ _effects.mcss   特效/动画
    |__ _grammer.mcss   语法增强
    |__ _help.mcss      辅助类
    |__ _text.mcss      文字类
    |__ _grid.mcss      布局
```


## _abstract 视觉类
**目录:**
```dir
_abstract
    |__ _unit
        |__ _arrow.mcss // css箭头
        |__ _btn.mcss   // 按钮
        |__ _cb.mcss    // checkbox
        |__ _crumb.mcss // 面包屑
        |__ _icon.mcss  // 图片和svg
        |__ _input.mcss // 输入框
        |__ _loading.mcss   // 载入等待
        |__ _rb.mcss    // radio
        |__ _textarea.mcss  // 多行输入框
        |__ _toast.mcss // 自由提示
        |__ _tooltip.mcss   // 工具提示
    |__ _mod
        |__ _form.mcss   // 表单相关
        |__ _tab.mcss    // tab选项
        |__ _modal.mcss  // 模态蒙层(通常嵌入form,也可以嵌入任何模块)
        |__ _carousel.mcss   // 轮播图
        |__ _menu.mcss  // 菜单相关
        |__ _select     // 下拉菜单
        |__ _steps.mcss // 分步走
        |__ _table.mcss // 表格
        |__ _progress.mcss  // 进度条
        
    |__ _grid
        |__ _cup.mcss   // 圣杯布局
        |__ _cols.mcss  // 多列布局
        |__ _horizontal.mcss // 水平居中
        |__ _vertical.mcss // 垂直居中
        |__ _hvcenter.mcss  // 水平和垂直居中
        |__ _fullscreen.mcss    // 全屏布局
```



## 业务样式

依赖:
```js

@import "(path)/mcss/_config/_import.mcss";     // 引入公共样式
@import "(path)/_globalMobi.mcss";              // 引入公共的业务样式,(举个例子)

```

实例样式代码:
```js
@extend abstractClassName;      //引入抽象类,增加的是选择符,不会导入实际代码;
@import realClassName;          //引入抽象类,增加的是实际代码;
```
