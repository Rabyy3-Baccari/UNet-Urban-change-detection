# Unsupervised Change Detection in Satellite Images Using Convolutional Neural Networks

## Overview
This project implements an unsupervised deep learning approach for detecting and classifying changes between satellite images of the same location taken at different times. The system utilizes a Convolutional Neural Network (CNN) architecture combined with semantic segmentation to automatically identify meaningful changes in satellite imagery.
![Unet](https://user-images.githubusercontent.com/48834483/54834087-1a4dfe80-4cc8-11e9-96bb-017fd63be742.png)

## Key Features
- Unsupervised change detection using CNN
- Semantic segmentation for change classification
- Difference image generation using CNN feature maps
- No requirement for manually labeled training data
- Automatic feature extraction and comparison

## Architecture
The project implements a U-Net architecture, which consists of:
- Encoding path (contracting): series of convolutional and max pooling layers
- Decoding path (expanding): series of up-convolutions and concatenations
- Skip connections: preserve spatial information at different scales

The U-Net architecture enables:
- Multi-scale feature extraction
- Precise localization
- Context awareness in change detection

## How It Works
1. Two satellite images of the same area at different times are input into the system
2. The CNN processes both images independently to extract feature maps
3. Feature maps are compared to generate a difference image
4. Semantic segmentation classifies detected changes
5. The system outputs both change detection and classification results

## Technical Details
### Requirements
- Python 3.6+
- PyTorch
- OpenCV
- NumPy
- GDAL (for satellite image processing)

### Input Data
- Satellite images (optical or multi-spectral)
- Images must be:
  - Co-registered
  - Of the same geographical area
  - Taken at different times

### Output
- Change detection map
- Semantic classification of changes
- Difference image visualization

## Results
The system has demonstrated effectiveness in detecting various types of changes:
- Urban development
- Deforestation
- Natural disasters impact
- Agricultural changes
- Infrastructure development

## Publications
- Research paper available on [ArXiv](https://arxiv.org/abs/1812.05815)
- Published in the proceedings of the IEEE International Joint Conference on Neural Networks, 2019

## Advantages
- No need for labeled training data
- Robust to seasonal variations
- Efficient processing of large-scale satellite imagery
- Automatic feature learning
- End-to-end trainable architecture


## Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation
```
@inproceedings{satelliteChangeDetection2019,
    title={Unsupervised Change Detection in Satellite Images Using Convolutional Neural Networks},
    author={}, # Add authors
    booktitle={2019 IEEE International Joint Conference on Neural Networks (IJCNN)},
    year={2019},
    pages={}, # Add page numbers
    organization={IEEE}
}
```

## Acknowledgments
- Thanks to the authors of the U-Net architecture
- IEEE International Joint Conference on Neural Networks
- All contributors and users of this project
