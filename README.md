# About this repo

一些nautilus里面用的脚本，需要的时候

```
mkdir ~/.local/share/nautilus/scripts
git clone https://github.com/jeffguorg/nautilus-scripts.git ~/.local/share/nautilus/scripts
```

重新打开你的nautilus，然后voila！看看你nautilus的上下文菜单

# Scripts

## convert

转换图片格式。脚本本身其实没做什么，无非是用OpenCV读取再保存成其他后缀名的图片。OpenCV会处理好格式这类事情。使用前记得建立软链接，比如说

```bash
ln -sv convert convert.jpg
```

右键你的图片，选择convert.jpg，就会把图片存成jpg格式

## fix-picture-ext

腾讯云的图片很古怪，备案的时候发现的，jpg拓展名的文件存的却是png格式的图片。所以用apache tika对python的binding，用tika猜测文件mime，然后按照mime改文件拓展名

## rotate

跟convert类似，用opencv旋转图片的
