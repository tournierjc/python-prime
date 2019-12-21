# python-prime
Script Python pour basculer entre NVIDIA PRIME et NVIDIA Offload

## Principe
Créer les fichiers de configuration X.Org pour basculer entre NVIDIA Prime et NVIDIA Offload. Devrait en principe fonctionner pour GNOME et KDE.

## Installation
Copier les fichiers dans les répertoires correspondants.
- `nvidia-prime` et `nvidia-offload` dans `/usr/bin/`
- `nvidia-prime.py`n nvidia-offload.py` et prime_switch.py` dans `/usr/share/prime-switch/`

S'assurer que le fichier de configuration dans `/etc/X11/xorg.conf.d/` s'appelle `10-nvidia-offload.conf` ou `10-nvidia-prime.conf`.
Créér un fichier `nvidia-drm.conf` contenant `options nvidia_drm modeset=1`. L'enregistrer dans `/etc/modprobe.d/`.


## Utilisation

Pour basculer entre les deux modes (attention cette manipulation va rédémarrer l'ordinateur): 
```
sudo nvidia-prime
```
```
sudo nvidia-offiload
```
