# 机器学习


## CNN

### 数据
1. 读取输入路径
   - 总的data_dir,加上train和valid
2. 数据增强和增多(data_transforms)
   - 用torchvison中transforms模块
   - 具体是指定'train/valid',transforms.Compose再加上具体的transforms.方法
3. 加载数据（image_datasets）
   - 利用datasets.ImageFolder读取路径
   - 加入transform
4. 载入batch（dataloaders）
   - batch和image_datasetsimage_datasets
5. 读入标签文件json

### 初始化模型
1. 指定model_name,feature_extract(是否只训练全连接层)
2. 指定GPU训练
   - train_on_gpu = torch.cuda.is_available()
   - device=torch.device()
3. 选择冻结的层（第一次训练把特征提取全部冻结，只训练全连接层）
  - 通过层的字典名字来选择冻结 
  ``` python 
  def set_parameter_requires_grad(model, feature_extracting):
    if feature_extracting:
        for name,param in model.parameters():
            if not 'fc' in name:
             param.requires_grad = False
  ```
1. 
