# 将VCCV转换为ARPAsing

PaintedCZ的英语VCCV录音方案在UTAU社区十分流行, 许多声库和UST都基于它.  当然, 它们也可被转换为ARPAsing格式来使用.

## 转换声库

英语VCCV声库可能会有"CC-", "CV_CVC"之类的子文件夹. 请将所有文件移至根目录下.  下载[这个]()索引文件, 重命名为"index.csv", 并放在根目录下.
完成后, 您便可以拖动声库文件夹到Moresampler上生成OTO了.  对于OTO中的重复项来说, **不要重命名, 也不要编号**.  可能会产生上百个重复项, 使ARPAsing Assistant无法正常运行.  下载[这个工具]()以便删除OTO中的重复项.  建议将参数的最大值设定在10-20之间.

## 转换UST

下载并解压[这个插件](), 将其放在UTAU安装目录内的Plugins文件夹中.  这个插件可以将UST中的Cz式音标转换为Arpabet音标.  但它目前还不能完全和ARPAsing声库兼容.  (比如有的音符可能会有2个以上的音标.)  您需要继续进行调校使其兼容ARPAsing声库.
原始插件由 ChieP 制作
转换器受 Ivory @TheIvoryShield 启发
插件由 KLAD 修改
