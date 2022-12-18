> LibreTranslate 是一个使用python开发的免费和开源的机器翻译API，完全是自我托管的。与其他API不同，它不依赖谷歌或Azure等专有供应商来进行翻译。相反，它的翻译引擎是由开源的Argos Translate库提供的。

可以在 https://libretranslate.com  在线试用翻译效果.
本人试验过,确实可以翻译,但出来的english->中文的翻译效果一言难尽,可以说不如人意.


以下介绍安装过程:

#### docker 安装

```
docker run -ti --rm -p 5000:5000 libretranslate/libretranslate
```

运行时出错,报:

```
Local package index not found, use package.update_package_index() to load it
Traceback (most recent call last):
  File "./venv/bin/libretranslate", line 33, in <module>
    sys.exit(load_entry_point('libretranslate==1.3.3', 'console_scripts', 'libretranslate')())
  File "/app/venv/lib/python3.8/site-packages/app/main.py", line 153, in main
    app = create_app(args)
  File "/app/venv/lib/python3.8/site-packages/app/app.py", line 142, in create_app
    frontend_argos_language_source = languages[0]
IndexError: list index out of range

```

看起来语言包没下载?没继续折腾,换个方法再试.

#### pip 安装

```
pip install libretranslate
```

安装顺利,执行时

```
libretranslate 
```

首次执行会去自动下载语言翻译模型,但非常的慢!
后来等的受不了,强制结束下载过程 (ctrl + c)

找到:
c:\users\用户名\.local\share\argos-translate\packages

删除这个目录里的所有文件,再去网站

https://www.argosopentech.com/argospm/index/ 手动下载语言包,比如我就下载了

en->ch 和 ch->en 两个包,解压缩后放到 c:\users\用户名\.local\share\argos-translate\packages 目录下

重新运行 :

```
libretranslate --load-only en,zh
```

这时再访问  http://localhost:5000 可以看到翻译页面,能进行翻译了





