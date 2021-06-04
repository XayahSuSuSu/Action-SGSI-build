# Action-SGSI-build

> 适配Android R
>
> 修复制作超过2G的SGSI无法上传Release的问题

## 快速开始

1. Fork此仓库
   
   首次使用时，你需要先**Fork此仓库**，然后再进行参数配置

2. 配置参数

   假设你此时已经Fork本仓库并进入自己的仓库，点击菜单中 **Settings - Secrets - New repository secret**
   
   按下表新建加密环境变量

   |说明               |Name       |Value(按你自己的需求填写)                                                 |
   |:------:           |:------:   | :------------------------:                                               |
   |待制作包链接       |ROM_URL    |https://hugeota.d.miui.com/21.5.31/miui_TUCANA_21.5.31_cb42ec9bed_11.0.zip|
   |待制作包名称       |ZIP_NAME   |miui_TUCANA_21.5.31_cb42ec9bed_11.0.zip                                   |
   |待制作包种类       |OS_TYPE    |miui                                                                      |
   |打包名称           |REPACK_NAME|SGSI.zip                                                                  |

## 后续步骤

由于[Github large binaries](https://docs.github.com/en/github/managing-large-files/working-with-large-files/distributing-large-binaries)限制，制作后的SGSI若超过**2GB**则**无法上传**，因此本Action将自动根据制作后的SGSI大小选择**直接上传**/**分卷上传**

若以分卷方式上传，请下载每个分卷后手动合卷解压

```
cat ${fileName}*>${fileName}.tar.gz    # 将分卷文件fileName*合并
tar xzvf ${fileName}.tar.gz            # 解压
```

## 版权与致谢

本项目受 [SGSI-build-action](https://github.com/xiaoxindada/SGSI-build-action) 项目启发。

感谢[xiaoxindada](https://github.com/xiaoxindada)的开源。
