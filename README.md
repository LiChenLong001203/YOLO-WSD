
1.Download the .rar project package to your local machine and download the WSODD dataset. The dataset link is: https://github.com/sunjiaen/WSODD.
2.Ensure the local Python environment and PyTorch framework are installed.
3.Modify the ultralytics-main/ultralytics/cfg/datasets/WSODD.yaml file to point to the dataset path. Replace the path with the absolute path where WSODD is stored on your computer.
4.Modify ultralytics-main/ceshi.py. You need to change three places in ceshi.py. Update ceshi.py to the following configuration:
ceshi.py需要修改三处：将ceshi.py修改为如下配置
model = YOLO('ultralytics-main/ultralytics/cfg/models/v8/yolov8n-all2.yaml')
    results = model.train(
        data='ultralytics/cfg/datasets/WSODD.yaml', epochs=150, )
    model.train(**{'cfg': 'ultralytics-main/ultralytics/cfg/default.yaml'})
5.之后在终端或本地运行ceshi.py即可。其余配置以及都修改好了






