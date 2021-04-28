# ARAS-LICENSE-PLATE-RECOGNITION
### Inicializar ambiente de conda
```
conda env create -f conda-gpu.yml
conda activate yolov4-gpu
```
### Correr el modelo
```
python save_model.py --weights ./data/custom.weights --output ./checkpoints/custom-416 --input_size 416 --model yolov4 
```
### Correr el detector en imagenes
```
python detect.py --weights ./checkpoints/custom-416 --size 416 --model yolov4 --images ./data/images/car5.jpg --plate
```
### Correr el detector en videos
```
python detect_video.py --weights ./checkpoints/custom-416 --size 416 --model yolov4 --video ./data/video/test4.mp4 --output ./detections/recognition.avi --plate
```
