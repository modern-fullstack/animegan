## PyTorch Implementation of [AnimeGANv2](https://github.com/TachibanaYoshino/AnimeGANv2)


**Updates**

* `2021-10-17` Add weights for [face portrait v2](https://github.com/bryandlee/animegan2-pytorch#additional-models)
* `2021-11-07` Thanks to [ak92501](https://twitter.com/ak92501), a web demo is integrated to [Huggingface Spaces](https://huggingface.co/spaces) with [Gradio](https://github.com/gradio-app/gradio). 
 
    See demo: [![Hugging Face Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Spaces-blue)](https://huggingface.co/spaces/akhaliq/AnimeGANv2)



**Weight Conversion from the Original Repo (Requires TensorFlow 1.x)**
```
git clone https://github.com/TachibanaYoshino/AnimeGANv2
python convert_weights.py
```

**Inference**
```
python test.py --input_dir [image_folder_path] --device [cpu/cuda]
```


**Results from converted [[Paprika]](https://drive.google.com/file/d/1K_xN32uoQKI8XmNYNLTX5gDn1UnQVe5I/view?usp=sharing) style model**

(input image, original tensorflow result, pytorch result from left to right)

<img src="./samples/compare/1.jpg" width="960"> &nbsp; 
<img src="./samples/compare/2.jpg" width="960"> &nbsp; 
<img src="./samples/compare/3.jpg" width="960"> &nbsp; 

**Note:** Training code not included / Tested on RTX3090 + PyTorch1.7.1 / Results from converted weights slightly different due to the [bilinear upsample issue](https://github.com/pytorch/pytorch/issues/10604)




## Additional Models

**Webtoon Face** [[ckpt]](https://drive.google.com/file/d/10T6F3-_RFOCJn6lMb-6mRmcISuYWJXGc)

<details>
<summary>samples</summary>

Trained on <b>256x256</b> face images. Distilled from [webtoon face model](https://github.com/bryandlee/naver-webtoon-faces/blob/master/README.md#face2webtoon) with L2 + VGG + GAN Loss and CelebA-HQ images. See `test_faces.ipynb` for details.

<img src="./samples/face_results.jpg" width="512"> &nbsp; 
  
</details>


**Face Portrait v1** [[ckpt]](https://drive.google.com/file/d/1WK5Mdt6mwlcsqCZMHkCUSDJxN1UyFi0-)

<details>
<summary>samples</summary>

Trained on <b>512x512</b> face images.

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jCqcKekdtKzW7cxiw_bjbbfLsPh-dEds?usp=sharing)
  
![samples](https://user-images.githubusercontent.com/26464535/127134790-93595da2-4f8b-4aca-a9d7-98699c5e6914.jpg)

[📺](https://youtu.be/CbMfI-HNCzw?t=317)
  
![sample](https://user-images.githubusercontent.com/26464535/129888683-98bb6283-7bb8-4d1a-a04a-e795f5858dcf.gif)

</details>


**Face Portrait v2** [[ckpt]](https://drive.google.com/uc?id=18H3iK09_d54qEDoWIc82SyWB2xun4gjU)

<details>
<summary>samples</summary>

Trained on <b>512x512</b> face images. Compared to v1, `🔻beautify` `🔺robustness` 

[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1jCqcKekdtKzW7cxiw_bjbbfLsPh-dEds?usp=sharing)
  
![face_portrait_v2_0](https://user-images.githubusercontent.com/26464535/137619176-59620b59-4e20-4d98-9559-a424f86b7f24.jpg)

![face_portrait_v2_1](https://user-images.githubusercontent.com/26464535/137619181-a45c9230-f5e7-4f3c-8002-7c266f89de45.jpg)

🦑 🎮 🔥
  
![face_portrait_v2_squid_game](https://user-images.githubusercontent.com/26464535/137619183-20e94f11-7a8e-4c3e-9b45-378ab63827ca.jpg)


</details>


