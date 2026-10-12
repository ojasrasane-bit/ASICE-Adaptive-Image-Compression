# ASICE — Adaptive Spatial Image Compression Engine

ASICE is an adaptive image compression project that focuses on preserving important regions of an image while reducing its storage requirements. Unlike conventional approaches that treat the entire image uniformly, ASICE identifies visually significant regions and applies different spatial compression strategies to the foreground and background.

## Key Features

- **Saliency Detection:** Uses a pretrained U²-Net model to identify visually important regions.
- **Region of Interest (ROI) Preservation:** Protects important image regions during compression.
- **Quadtree Decomposition:** Divides images into smaller blocks based on their spatial characteristics.
- **Dynamic Programming-Based Tiling:** Optimizes the arrangement of eligible background blocks.
- **Conditional Huffman Coding:** Applies entropy coding when the target compression ratio has not been reached.
- **Batch Processing:** Supports processing individual images and directories of images.
- **Custom Archive Format:** Uses the proposed `.asice` format to store encoded image data and reconstruction metadata.

## Technology and Algorithms

- Python
- Deep Learning and Computer Vision
- U²-Net Saliency Detection
- Quadtree Decomposition
- Dynamic Programming
- Huffman Coding
- Image Compression and Reconstruction

## Project Objective

The goal of ASICE is to investigate how content-aware compression can reduce image storage requirements while preserving important visual information. The system evaluates compression ratio, ROI reconstruction accuracy, background reconstruction error, and processing time.

## Evaluation

The current research implementation was evaluated on a custom wallpaper dataset and a subset of the COCO dataset. The reported results achieved exact reconstruction of protected ROI pixels in both datasets. However, the target compression ratio of 4:1 and the runtime target remain areas for further optimization.

## Future Improvements

- Improve compression efficiency for already-compressed image formats.
- Optimize processing time and computational overhead.
- Conduct parameter sensitivity and component-wise ablation studies.
- Improve decoder validation and archive compatibility.
- Explore transform-based compression for background regions.

## Research Contribution

ASICE explores the integration of saliency-guided ROI protection, spatial decomposition, block optimization, and conditional entropy coding in a single adaptive image compression pipeline.

**Note:** This project is a work in progress, and reported performance targets should not be interpreted as fully achieved results.
