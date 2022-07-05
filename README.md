# AlphaPose Using YOLOX

Original AlhpaPose : https://github.com/MVIG-SJTU/AlphaPose


YOLOX : https://github.com/Megvii-BaseDetection/YOLOX

# Edited in AlphaPose
 - Detector : YOLOv3 => YOLOX 
 - Detector_NMS : YOLOXv3 => YOLOX
 - Detected Object : Only Human => All COCO object
 - PoseNMS for object class not human
 - Writer write json_file for all object
 - Save Image for object bounding box no Skeleton


## YOLOv3
![0005_c6_f0030883](https://user-images.githubusercontent.com/60573146/171554274-bb57608c-2f3a-48ca-a401-0960c5ab5f22.jpg) 
![0031_c2_f0062046](https://user-images.githubusercontent.com/60573146/177261242-215c98b1-20e9-4ade-8997-ed1202fc8aa8.jpg)

<br>

## YOLOX
![0005_c6_f0030883](https://user-images.githubusercontent.com/60573146/171554245-e929d584-c66c-4915-bf6d-d418e7c7e715.jpg) 
![0031_c2_f0062046](https://user-images.githubusercontent.com/60573146/177261368-a19ed53c-047f-4687-8422-ab5201d90a7f.jpg)


# AlphaPose with YOLOv3 보다 개선된 점
- Bounding Box 개선
- Bounding Box가 개선되면서 PoseEstimation 부분에 더 정확한 Bounding Box가 넘어가게 됨으로써 Skeleton 개선
- Object Detection 추가
- Detector 하이퍼파라미터 조절 가능


# Install
<pre>
<code>
git clone https://github.com/HJSIFEN/YOLOX_X_AlphaPose.git
cd yolox_x_alphapose
python setup.py build develop
</code>
</pre>


# Demo Inference

datasize : ["yolox_s", "yolox_m", "yolox_l", "yolox_m"]
<pre>
<code>
python scripts/demo_inference.py --cfg ./configs/coco/resnet/256x192_res50_lr1e-3_1x.yaml --checkpoint ./pretrained_models/fast_res50_256x192.pth --indir {input_dir} --outdir {output_dir} --save_img --showbox --conf 0.1 --nms 0.6 --model_size "yolox_x"
</code>
</pre>


## AlphaPose License
AlphaPose is freely available for free non-commercial use, and may be redistributed under these conditions. For commercial queries, please drop an e-mail at mvig.alphapose[at]gmail[dot]com and cc lucewu[[at]sjtu[dot]edu[dot]cn. We will send the detail agreement to you.

for commercial queries you must contact AlphaPose developer
