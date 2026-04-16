# Soccer Player Re-Identification

Computer vision pipeline that detects and re-identifies soccer players 
across frames and camera angles using deep appearance embeddings.

## What it does
- Detects players in match footage using YOLO
- Re-identifies the same player across frames using similarity matching
- Handles occlusion, jersey similarity, and motion blur
- Outputs visualized tracking on match clips

## Tech Stack
Python · PyTorch · YOLO · OpenCV

## Architecture
1. YOLO detector → player bounding boxes per frame  
2. Appearance embedding model → feature vector per crop  
3. Cosine similarity → identity association across frames  
4. Visualization → tracked output video

## Challenges solved
- Jersey similarity between players (same team colors)
- Motion blur during fast movement
- Partial occlusion handling

## Run
```bash
pip install -r requirements.txt
python track.py --input match_clip.mp4
```
