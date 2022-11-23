## POC 

### Universidad - Asignatura
Universidad Tecnologica Nacional - Seminario


### Proposito del test
Comprobar la identificacion de 2 objetos distintos en una imagen

### Informacion de tecnologia utilizada
Red convolucional yolov5 con un modelo preentrenado\
Se realizo con google colaboratory

### Informacion de ejecucion
La notebook posee una grabacion de una instancia de ejecucion que demuestra su correcto funcionamiento\
* Para probar la generacion de la red y la posterior prueba se debe ejecutar secuencialmente desde 0\
* Para probar la ya generada con la imagen precargada:\
* * https://colab.research.google.com/drive/1QTXKy8xGK79bVQIIPQDRS0m51ykjWadb#scrollTo=b006PFd7d33V&line=10&uniqifier=1
```
from IPython.display import Image
%cd /content
generatedWeights = f"https://github.com/melinaceleg/CNNPOC/raw/main/best.pt"
!wget --no-cache --backups=1 {generatedWeights}
image = f"https://github.com/melinaceleg/CNNPOC/raw/main/img.jpg"
!wget --no-cache --backups=1 {image}
!python detect.py --source content/img.jpg --weights content/yolov5/poc2classes/exp/weights/best.pt --conf 0.25

%cd yolov5/runs/detect
Image('img.jpg')
```

### Requerimientos de eficiencia en la identificacion de los objetos
Desde 0.6 











