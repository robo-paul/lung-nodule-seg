# lung-nodule-seg
lung-nodule-segmentation tool using attention-unet and gradio
---
title: Lung Nodule Segmentation
emoji: 🫁
colorFrom: blue
colorTo: red
sdk: gradio
sdk_version: 5.39.0
app_file: app.py
pinned: false
license: mit
---

# Lung Nodule Segmentation with Attention UNet

This space segments lung nodules from CT scan slices using an Attention UNet model.

## Features

- 🖼️ **Multiple format support**: PNG, JPG, JPEG, BMP, TIFF
- 📊 **MHD medical format**: Directly process .mhd files
- 🎯 **Automatic slice selection**: For 3D volumes
- 🏥 **CT windowing**: Optimized lung window settings
- 📈 **Interactive visualization**: Overlay and metrics

## Usage

1. Wait for the model to load (first time may take a moment)
2. Upload a CT image or MHD file
3. Adjust the threshold if needed
4. Click "Segment Nodules"
5. View results in the tabs

## Model Architecture

- **Type**: Attention U-Net
- **Input**: 1-channel grayscale (512×512)
- **Output**: Binary segmentation mask
- **Parameters**: ~8 million
- **Training**: LUNA16 dataset

## Technical Details

- MHD files are processed with SimpleITK
- CT windowing: Center=40, Width=400 (lung window)
- Default slice: Middle slice of 3D volume
- Image resizing: 512×512 pixels

## File Structure
