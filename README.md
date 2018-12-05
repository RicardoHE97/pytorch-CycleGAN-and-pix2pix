# Sketch2shiba

Este proyecto fue forkeado de [pix2pix y CycleGAN](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix) y su proposito es que a base de un dibujo o bosquejo de un perro la red genere un perro de raza Shiba inu. En mi [blog](https://ricardohe97.github.io/post/sketch2shiba/) describo mejor el proceso y como funciona esta red.

Este proyecto es parte de la evaluación de la mitad de curso de la materia de Redes neuronales de la Univerisdad de Sonora

## Prerequisitos
* Linux o macOS
* Python 2 o 3
* CPU o NVIDIA GPU + CUDA CuDNN


## Instalación

* Clonar este repositorio
```bash
git clone https://github.com/RicardoHE97/sketch2shiba
cd sketch2shiba
```

* Instalar PyTorch 0.4+ y torchvision de http://pytorch.org y otras dependencias (e.g., [visdom](https://github.com/facebookresearch/visdom) y [dominate](https://github.com/Knio/dominate)). Se pueden instalar todas las dependencias así:
```bash
pip install -r requirements.txt
```

* Para usuarios de Conda, los autores incluyeron un script `./scripts/conda_deps.sh` para instalar PyTorch y otras librerias

## Aplicar el modelo

* Crear una carpeta `checkpoints` en la carpeta raíz del proyecto

* En este [enlace](https://correoauson-my.sharepoint.com/:u:/g/personal/a215208421_alumnos_unison_mx/ERZWhnhAOy9ClzszkQHhCYcB9qgLZse0k2uJ7_gdbW8B7Q?e=hgTJkH) se puede descargar la red que genera shibas inu para que tu generes tus propios perro.

* Una vez descargado, se deben mover la carpeta `sketch2shibaV2_unet_256` a la carpeta `checkpoints/`

* El proyecto ya cuenta con un conjunto de datos preparados para entrenar y probar el modelo

* Para probar el modelo se debe correr el siguiente comando
```bash
python test.py --dataroot ./datasets/sketch2shibaV2/ --direction AtoB --model pix2pix --name sketch2shibaV2_unet_256
```
* Si no se cuenta con un GPU entonces se debe agregar la siguiente opción al comando anterior `--gpu_ids -1`

* Los resultados estaran en la carpeta `results/sketch2shibaV2_unet_256/`
## Modelos generados
[sketch2shiba-Unet256](https://correoauson-my.sharepoint.com/:u:/g/personal/a215208421_alumnos_unison_mx/ERZWhnhAOy9ClzszkQHhCYcB9qgLZse0k2uJ7_gdbW8B7Q?e=hgTJkH)
