# 作业5文物视觉问答对接下载

本仓库用于向合作同学交接已经完成的文物识别项目资源。两个资源包放在Release附件中，无需克隆仓库。

## 下载

| 文件 | 大小 | 内容 |
|---|---:|---|
| [基础对接包](https://github.com/Sunnyanan/vqa-homework-handoff/releases/download/vqa-handoff-2026-11-12/vqa-handoff-core-2026-11-12.zip) | 约349 MiB | 故宫文物图像、标签、来源、固定划分、两个分类模型、推理依赖、对接文档及报告 |
| [检测扩展包](https://github.com/Sunnyanan/vqa-homework-handoff/releases/download/vqa-handoff-2026-11-12/vqa-handoff-detection-2026-11-12.zip) | 约965 MiB | Kasteev Museum场景图、检测标签与划分、37展品YOLOv8s模型及结果 |
| [SHA256校验清单](https://github.com/Sunnyanan/vqa-homework-handoff/releases/download/vqa-handoff-2026-11-12/SHA256SUMS) | 小文件 | 核对两个ZIP是否完整 |

也可以打开[本次Release](https://github.com/Sunnyanan/vqa-homework-handoff/releases/tag/vqa-handoff-2026-11-12)，在Assets中选择下载。自动生成的Source code压缩包不能替代上面的两个资源包。

## 使用

1. 将基础包解压到一个新建项目目录。
2. 需要真实博物馆场景检测时，将检测扩展包也解压到同一个目录。
3. 阅读根目录的包使用说明，再看reports中的《文物识别与多模态视觉问答_对接文档》。
4. 按包内说明安装环境，先跑验证样例，再开展VQA数据标注与多模态训练。

ZIP中的原目录结构需要保留；同名best.pt不能放到同一层。包内另有逐文件校验清单。

## 数据与评价范围

- 故宫粗分类：1,497张、15类；训练/验证/测试1,047/225/225；固定ResNet50测试准确率87.56%。
- 陶瓷细分类：299张、碗/盘/瓶/罐/杯；划分209/45/45；固定ResNet50测试准确率88.89%。
- 基础包共1,796个有效样本，同时保留403张对应的预处理图，共2,199个图像文件。原图与处理图是同一样本的不同版本。
- Kasteev：源图4,128张，实验划分2,462/629/633；403张间隔帧及1张排除重复图不参与三集合。按manifest中的split选图。
- Kasteev的37类是具体展品身份；固定测试mAP50为98.96%，属于同源拍摄内部帧块留出，不代表新馆、新视频或未知展品泛化。

本交接不包含已标注好的1,000组文物VQA、完整多模态问答模型或已验证的联合问答准确率。问答组需继续完成相应工作。

## 来源与版本

资源基于2026-10-28冻结课程成果，交接包整理于2026-11-12。馆藏来源记录、署名及许可说明保留在包内；以各数据来源的条件为准。

这里只维护下载入口和说明，后续资源变更使用新的Release及校验值。
