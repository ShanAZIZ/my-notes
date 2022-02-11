# Configurer les ecrans externes 

__source__ : [qastack.fr](https://qastack.fr/ubuntu/393400/is-it-possible-to-have-different-dpi-configurations-for-two-different-screens)

Maintenant, j'utilise Ubuntu 14.10 & GNOME Shell 3.12.2, qui offre un support HiDPI assez utilisable. Donc, j'utilise simplement le support prêt à l'emploi de HiDPI - le facteur de mise à l'échelle est 2 (il peut être configuré via une interface graphique). Cela signifie que sur un moniteur externe, tout est deux fois plus grand que ce qui est acceptable. Ainsi, j'utilise xrandr; mais au lieu de réduire la taille de l'écran d'un ordinateur portable, j'augmente l'écran du moniteur externe:


```xrandr --output HDMI1 --scale 2x2 --mode 1920x1200 --fb 3840x4200 --pos 0x0```

```xrandr --output eDP1 --scale 1x1 --pos 320x2400```

Donc, un par un:

```--output HDMI1 ``` dans mon cas, c'est l'écran externe, eDP1c'est l'écran du portable.

```--scale 2x2 ``` rendre tout sur l'écran externe deux fois plus petit

```--mode XxY``` régler explicitement la résolution pour l'écran (pas nécessaire si est déjà défini)

```--fb XxY``` Définir la taille d'un écran virtuel (framebuffer) ( important sans cela, vous ne pourrez utiliser qu'une quatrième partie de l'écran). Dans mon cas, les écrans se superposant, j’ai donc ajouté les hauteurs effectives 2400 + 1800 = 4200. Notez également que la taille maximale du framebuffer peut être spécifiée dans xorg.conf - vous ne pouvez pas la dépasser (elle est écrite dans la première ligne de xrandr -qsortie).

```--pos XxY``` Dans mon cas, je règle le positionnement absolu des écrans, de sorte que l'écran de mon ordinateur portable se trouve directement au bas de l'écran externe. La valeur Y est le double de la hauteur du moniteur externe.