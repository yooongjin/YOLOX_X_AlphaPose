# AlphaPose with yolov3 => yolox

Original AlhpaPose : https://github.com/MVIG-SJTU/AlphaPose

## ■ YOLOv3  →  YOLOX
![0005_c2_f0046985](https://user-images.githubusercontent.com/60573146/171554270-dd65d156-ff8c-4dcd-ba00-5f4deaf78c1b.jpg)
![0005_c6_f0030883](https://user-images.githubusercontent.com/60573146/171554274-bb57608c-2f3a-48ca-a401-0960c5ab5f22.jpg)
![0019_c1_f0051470](https://user-images.githubusercontent.com/60573146/171554284-494a600b-ccde-41dc-9b3e-75ff1917ed51.jpg)
→→→
![0005_c2_f0046985](https://user-images.githubusercontent.com/60573146/171554197-379f44e2-3344-4616-82d1-d0458f05e2b0.jpg)
![0005_c6_f0030883](https://user-images.githubusercontent.com/60573146/171554245-e929d584-c66c-4915-bf6d-d418e7c7e715.jpg)
![0019_c1_f0051470](https://user-images.githubusercontent.com/60573146/171554259-117d06d7-2732-4358-8231-64c98a0db5e7.jpg)

### 개선점
- Bounding Box 개선
- Skeleton 개선
- Object Detection 추가

<pre>
<code>
python scripts/demo_inference.py --cfg ./configs/coco/resnet/256x192_res50_lr1e-3_1x.yaml --checkpoint ./pretrained_models/fast_res50_256x192.pth --indir "C:\Users\user\Desktop\RE-ID\datasets\DukeMTMC-reID\query" --outdir examples/yolox_x/all --save_img --showbox --conf 0.1 --nms 0.6 --model_size "yolox_x"
</code>
</pre>
