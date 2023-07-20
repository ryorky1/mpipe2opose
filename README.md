<a name="readme"></a>

<!-- [![Contributors][contributors-shield]][contributors-url] -->
![Python][python-shield]

<!-- GETTING STARTED -->

# MediaPipe Pose to OpenPose JSON
## Info

Mediapipe pose extraction and exporting to OpenPose format but Mediapipe has 33 keypoints as output as compared to 25 from Openpose. The keypoints also have a different order.  This script resolves the issues
The code in this repository has three scripts:
- `mediapipe_JSON.py` :  extracts the keypoints from all images in a folder and exports them as an Openpose JSON format with 25 keypoints. The JSON is compaitble with SMPLify-X for 3D shape extraction.
- `plot_json.py` : plots the OpenPose keypoints and saves the image. (not required)


## Limitations:
- Supports only 1 person per frame (Mediapipe limitation)
- Supports multiple image extensions in folder (PNG, JPG, JPEG etc)

## Requirements
To install all the required packages: `pip install -r requirements.txt`  (preferabale if usung python 11) or `pip install -r requirements-initial.txt` (if using lower python version)

## File Locations
 - Input images Location: `data/input`
 - Moved Input Image Location after processing: `data/output/moved_image`
 - Mediapipe Image Skeleton after processing: `data/output/mpipe_skeleton_img` 
 - Openpose Keypoints File after processing: `data/output/opose_json`
 - Hydra Logs/Json logs storage location: `outputs/...`

## Config Updates required
 - Update `src/conf/config.yaml` to match necessary paths

