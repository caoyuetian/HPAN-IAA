# Vessel re-identification by a {HIERARCHICAL PERCEPTUAL AGGREGATION NETWORK} with {INCLINATION-AWARE ATTENTION}
## 1.Abstract
Vessel re-identification is a crucial task in maritime supervision. However,distinct from land-based scenarios involving vehicles or pedestrians, vessels, as enormous rigid bodies situated in the dynamic marine environment, face unique challenges such as significant variations in the scale of discriminative features and unpredictable sway.Furthermore, there is a limited number of publiclyavailable datasets for vessel re-identification in complex backgrounds. In this paper, to overcome these challenges, a novel Hierarchical Perceptual Aggregation Network with Inclination-Aware Attention (HPAN-IAA) is proposed. HPANIAA comprises two main modules: the Hierarchical Perceptual Aggregation Block (HPAB) and the Inclination-Aware Attention Block (IAAB). Specifically,in HPAB, a hierarchical perceptual function is introduced to decompose visual information of vessels into discriminative features at multiple levels. These feature maps with different levels of detail from diverse network layers are then fused together by concatenation, resulting in a comprehensive feature representation that effectively integrates information across various scales.Conversely, to address the irregular variations and random omissions in discriminative feature distribution caused by unpredictable vessel sway, in IAAB, the Channel Collaborative Attention Module (CCAM) and the Pyramidal Spatial Attention Module (PSAM) are designed to adaptively extract potential discriminative features within each channel and spatial dimension, enhancing model’s ability in effectively extracting and utilizing irregularly changing discriminative features.Moreover, we propose a novel vessel re-identification dataset- VesselReID-2258. Extensive experiments conducted on VesselReID-2258 and the publicly available dataset VesselReID demonstrate that HPAN-IAA outperforms the current state-of-the-art by up to 0.002 and 0.04 respectively in mean average precision (mAP).

## 2.The structure of the HPAN-IAA
![image](https://github.com/user-attachments/assets/6e3f2ea5-e311-46b5-a5d6-5c0b687a3165)

The images are passed through the ResNet50, and each layer generates a three-dimensional feature map. The HPAB utilizes a hierarchical pooling function to process the feature
maps emanating from the distinct layers of the model. It allows for the capture of hierarchical features, ensuring the richness and diversity of the features. The IAAB focuses on the crucial features of each layer of the network using Channel Collaborative Attention Module and Pyramidal Spatial Attention Module.

## 3.VesselReID-2258 dataset
![6](https://github.com/user-attachments/assets/4727733c-3a64-4501-b99a-990c231b5d98)
Images of partial vessels in the VesselReID- 2258 dataset, with every row presenting an image of the selected vessel’s identification.

![image](https://github.com/user-attachments/assets/a7c00f9d-2b9c-4802-909d-e792347277fc)

Our dataset comprises eight major vessel types, including a total of 122,477 images of 2,258 vessels. On average, each vessel has approximately 50 images. The dataset includes 172 Cargo Ships, 443 Fishing Boats, 375 High-Speed Ships, 36 Navigation Aid Ships, 195 Passenger Ships, 333 Pleasure Craft Ships, 223 Tankers, and 481 Tug & Special Craft Ships.


