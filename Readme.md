#  hexo-deployer-aliyun-oss部署器使用说明

本项目：https://github.com/arkylin/hexo-deployer-aliyun-oss

源项目：https://github.com/wertycn/hexo-deployer-ali-oss

**本项目**在**源项目**的基础上**增加**了**MD5校验工具**，这样就可以避免上传重复文件耗时了，本地计算MD5的时间如果不是什么大文件，基本可以忽略不计，后续也可能会加入其他功能。例如：文件排除项、时间或文件大小比对等

在hexo项目下执行安装命令：

```
    npm install hexo-deployer-aliyun-oss --save
```

在hexo项目配置文件`_config.yml`中添加如下配置：

```
deploy:
  type: ali-oss
  region: <您的oss 区域代码>
  accessKeyId: <您的oss  accessKeyId>
  accessKeySecret: <您的oss accessKeySecret>
  bucket: <您的bucket name>
  
```

就这么简单 然后执行部署命令：

```
hexo d
```

即可将项目部署到oss中 ，默认情况下，将文件上传到bucket的根目录下，如果需要部署到其他目录，请在deploy下添加remotePath选项进行指定

```
	remotePath:<您要部署的目录>
```