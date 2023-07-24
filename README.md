
## Training

```bash
    CUDA_VISIBLE_DEVICES=3 python train_3d.py --outdir "/data/jayeon/Trained/get3d/test/" --data "/data/jayeon/Dataset/Get3D/RenderedData/img/02958343/" --camera_path "/data/jayeon/Dataset/Get3D/RenderedData/camera" --gpus=1 --batch=4 --gamma=40 --use_shapenet_split 1 --fp32 0 --metrics=""
```

## Evaluation Matrix

```bash
    CUDA_VISIBLE_DEVICE=2 python train_3d.py --outdir "/data/jayeon/Trained/get3d/" --data "/data/jayeon/Dataset/Get3D/RenderedData/img/02958343/" --camera_path "/data/jayeon/Dataset/Get3D/RenderedData/camera" --gpus=1 --batch=4 --gamma=40 --use_shapenet_split 1 --fp32 0 --metrics "fid50k_full" --inference_vis 1 --resume_pretrain "" --inference_to_generate_textured_mesh 1 --inference_compute_fid 1 --inference_generate_geo 1
```