我们需要面向电商场景实现根据模特照片搜寻相关商品的功能，因此需要搭建一个电商搜索引擎。

由于模特图和商品图都很脏，因此我们需要预先对图片进行分割，然后再使用多模态embedding模型进行向量化，然后使用VikingDB实现存储，最后利用Gradio实现可视化demo，此外还需要对正确率进行一个计算，预计需要达到70%以上。

# 技术选型

1. 图像分割：[ségformer_b2_clothes](https://huggingface.co/mattmdjaga/segformer_b2_clothes)
2. 多模态embedding：[bge-visualized-m3](https://huggingface.co/BAAI/bge-visualized)
3. 向量存储：[VikingDB](https://www.volcengine.com/docs/84313/1254439)
4. 可视化demo：[Gradio](https://github.com/gradio-app/gradio)

# 项目结构
test_fuc文件夹下主要为功能测试的代码，包括图像分割、多模态embedding、向量存储、可视化demo等。

test_img文件夹下为测试图片，包括模特照片和商品照片。