<div align="center">
	<span style="font-weight: bold"> English | <a href=README_CN.md> 中文 </a> </span>
</div>

# Action-SGSI-build

> Adapt to Android R
>
> Fix the issue that release cannot be uploaded to SGSI made with more than 2G
>
> Support custom streamlining functions
>
> Current version: [v11](https://github.com/xiaoxindada/SGSI-build-tool/tree/11)
>
> Note: If the message fails and when downloading ROM... Error: Process completed with exit code 127. It is a server network problem, please try again

## Quick start

1. Fork this warehouse
   
   When you use it for the first time, you need to **Fork this warehouse**, and then configure the parameters

2. Configuration parameters

   Assuming that you have already Fork this warehouse and entered your own warehouse at this time, click Actions in the menu-SGSI_Build under All workflows in the left column-Run workflow gray button on the right-fill in the corresponding parameters

   |Description |Name |Value (fill in according to your own needs) |
   |:------: |:------: | :------------------------: |
   |Link to package to be made |ROM_URL |https://hugeota.d.miui.com/21.5.31/miui_TUCANA_21.5.31_cb42ec9bed_11.0.zip|
   |Package name to be made |ZIP_NAME |miui_TUCANA_21.5.31_cb42ec9bed_11.0.zip |
   |Type of package to be made |OS_TYPE |miui |
   |Package name |REPACK_NAME|SGSI.zip |

3. Start production
   
   Click the Run workflow green button to start production

## Personalized configuration

1. Customize and streamline functions
   
   Modify the simplified script of the corresponding system in the apps_clean folder, please refer to the modification by yourself

## Next steps

Due to the limitation of [Github large binaries](https://docs.github.com/en/github/managing-large-files/working-with-large-files/distributing-large-binaries), if the SGSI after production exceeds* *2GB** then **cannot upload**, so this Action will automatically select **Direct upload**/**Sub-volume upload** according to the size of the SGSI after production.

If uploading in sub-volumes, please download each sub-volume and manually unzip it

```
cat ${fileName}*>${fileName}.tar.gz    # merge the sub-volume file fileName*
tar xzvf ${fileName}.tar.gz            # Unzip
```

## Copyright and Acknowledgements

This project is inspired by the [SGSI-build-action](https://github.com/xiaoxindada/SGSI-build-action) project.

Thanks to [xiaoxindada](https://github.com/xiaoxindada) for the open source.‌‌
