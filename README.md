# Robot-learning-via-human-egocentric-vision
This is a repository for storing project-related papers 
## 🔥 News
Last update on 2024/08/28

## :hammer: Abstract
Embodied learning for object-centric robotic manipulation is a rapidly developing and challenging area in embodied AI. It is crucial for advancing next-generation intelligent robots and has garnered significant interest recently. Unlike data-driven machine learning methods, embodied learning focuses on robot learning through physical interaction with the environment and perceptual feedback, making it especially suitable for robotic manipulation. In this paper, we provide a comprehensive survey of the latest advancements in this field and categorize the existing work into three main branches: 1) Embodied perceptual learning, which aims to predict object pose and affordance through various data representations; 2) Embodied policy learning, which focuses on generating optimal robotic decisions using methods such as reinforcement learning and imitation learning; 3) Embodied task-oriented learning, designed to optimize the robot's performance based on the characteristics of different tasks in object grasping and manipulation. In addition, we offer an overview and discussion of public datasets, evaluation metrics, representative applications, current challenges, and potential future research directions.

## :pencil: Citation

```bib
@article{zheng2024ocrm,
  author= {Zheng, Ying and Yao, Lei and Su, Yuejiao and Zhang, Yi and Wang, Yi and Zhao, Sicheng and Zhang, Yiyi and Chau, Lap-Pui},
  title= {A Survey of Embodied Learning for Object-Centric Robotic Manipulation},
  journal={arXiv preprint arXiv:2408.11537},
  year={2024}
}
```
- [Awesome Object-Centric Robotic Manipulation](#awesome-object-centric-robotic-manipulation)
  - [🔥 News](#-news)
  - [:hammer: Abstract](#hammer-abstract)
  - [:pencil: Citation](#pencil-citation)
  - [Embodied Perceptual Learning](#embodied-perceptual-learning)
    - [Data Representation](#data-representation)
      - [Image-Based Representation](#image-based-representation)
      - [3D-Aware Representation](#3d-aware-representation)
      - [Tactile-Based Representation](#tactile-based-representation)
    - [Object Pose Estimation](#object-pose-estimation)
      - [Instance-Level Object Pose Estimation](#instance-level-object-pose-estimation)
      - [Category-Level Object Pose Estimation](#category-level-object-pose-estimation)
      - [Novel Object Pose Estimation](#novel-object-pose-estimation)
    - [Affordance Learning](#affordance-learning)
      - [Affordance Learning by Supervised Learning](#affordance-learning-by-supervised-learning)
      - [Affordance Learning From Interaction](#affordance-learning-from-interaction)
  - [Embodied Policy Learning](#embodied-policy-learning)
    - [Policy Representation](#policy-representation)
      - [Explicit Policy](#explicit-policy)
      - [Implicit Policy](#implicit-policy)
      - [Diffusion Policy](#diffusion-policy)
    - [Policy Learning](#policy-learning)
      - [Reinforcement Learning](#reinforcement-learning)
      - [Imitation Learning](#imitation-learning)
      - [Other Methods](#other-methods)
  - [Embodied Task-Oriented Learning](#embodied-task-oriented-learning)
    - [Object Grasping](#object-grasping)
      - [Single-Object Grasping](#single-object-grasping)
      - [Multi-Object Grasping](#multi-object-grasping)
    - [Object Manipulation](#object-manipulation)
      - [Non-Dexterous Manipulation](#non-dexterous-manipulation)
      - [Dexterous Manipulation](#dexterous-manipulation)
  - [Datasets](#datasets)
    - [Datasets for Object Grasping](#datasets-for-object-grasping)
    - [Datasets for Object Manipulation](#datasets-for-object-manipulation)
  - [Applications](#applications)
    - [Industrial Robots](#industrial-robots)
    - [Agricultural Robots](#agricultural-robots)
    - [Domestic Robots](#domestic-robots)
    - [Surgical Robots](#surgical-robots)
    - [Other Applications](#other-applications)
  - [Challenges and Future Directions](#challenges-and-future-directions)
    - [Sim-to-Real Generalization](#sim-to-real-generalization)
    - [Multimodal Embodied LLMs](#multimodal-embodied-llms)
    - [Human-Robot Collaboration](#human-robot-collaboration)
    - [Model Compression and Robot Acceleration](#model-compression-and-robot-acceleration)
    - [Model Interpretability and Application Safety](#model-interpretability-and-application-safety)
  - [:books: License](#books-license)
 
## Embodied Perceptual Learning
### Data Representation
#### Image-Based Representation
| Paper                    |  Venue | Code/Project |                                  
|---------------------------------------------|:-------------:|:------------:|
|[Real-time seamless single shot 6d object pose prediction](https://openaccess.thecvf.com/content_cvpr_2018/papers/Tekin_Real-Time_Seamless_Single_CVPR_2018_paper.pdf)|CVPR 2018|-|
|[MonoGraspNet: 6-DoF Grasping with a Single RGB Image](https://arxiv.org/pdf/2209.13036)|ICRA 2023|-|
|[RGBGrasp: Image-based Object Grasping by Capturing Multiple Views during Robot Arm Movement with Neural Radiance Fields](https://arxiv.org/pdf/2311.16592)|RAL 2024|[Project](https://sites.google.com/view/rgbgrasp)|
|[RGBManip: Monocular Image-based Robotic Manipulation through Active Object Pose Estimation](https://arxiv.org/pdf/2310.03478)|ICRA 2024|[Project](https://rgbmanip.github.io/)|
|[Evo-NeRF: Evolving NeRF for Sequential Robot Grasping of Transparent Objects](https://openreview.net/forum?id=Bxr45keYrf)|CoRL 2022|[Project](https://sites.google.com/view/evo-nerf)|
|[Clear-Splatting: Learning Residual Gaussian Splats for Transparent Object Manipulation](https://openreview.net/forum?id=HcUC6hGcwu)|ICRAW 2024|-|


#### 3D-Aware Representation
Depth-based representations
| Paper                    |  Venue | Code/Project |                                  
|---------------------------------------------|:-------------:|:------------:|
|[RGB-D object detection and semantic segmentation for autonomous manipulation in clutter](https://arxiv.org/pdf/1810.00818)|IJRR 2018|-|

Point cloud-based representations
| Paper                    |  Venue | Code/Project |                                  
|---------------------------------------------|:-------------:|:------------:|
|[Shape completion enabled robotic grasping](https://arxiv.org/pdf/1609.08546)|IROS 2017|-|
|[PointNetGPD: Detecting Grasp Configurations from Point Sets](https://arxiv.org/pdf/1809.06267)|ICRA 2019|[Project](https://lianghongzhuo.github.io/PointNetGPD/)|
|[3D Implicit Transporter for Temporally Consistent Keypoint Discovery](https://openaccess.thecvf.com/content/ICCV2023/html/Zhong_3D_Implicit_Transporter_for_Temporally_Consistent_Keypoint_Discovery_ICCV_2023_paper.html)|ICCV 2023|[Code](https://github.com/zhongcl-thu/3D-Implicit-Transporter)|
