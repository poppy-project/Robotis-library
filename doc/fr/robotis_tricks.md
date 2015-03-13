# /!\ Robotis Dynamixel : piège pour les débutants

Lorsque vous souhaitez assembler un Poppy, la première chose dont il faut vous assurer **est que vous assemblez correctement le palonnier des moteurs Dynamixel**. C'est à la fois la première étape et peut-être la plus critique. Une erreur dans la configuration ou l'assemblage de cette étape sera véritablement difficle à changer une fois que Poppy sera assemblé.

## 1. Gérer le palonnier sur le moteur
**ATTENTION ! Cette étape est critique !**

Les moteurs Dynamixel sont vendu non assemblés, vous aurez à ajouter manuellement le palonnier HN07-N101 (pour le modèle MX-28) et HN05-N102 (pour le modèle MX-64).
Le point critique est de placer le palonnier correctement, sur la position zéro. Pour le faire, vous aurez à aligner correctement la marque de poinçon de l'arbre avec l'entaille de le palonnier :

<img src="../img/robotis_dynamixel_axe_mark.jpg" height="300"> <img src="../img/robotis_horn_mark.jpg" height="300">

Quand montée, le palonnier est véritablement difficile à enlever et vous aurez certainement à endommager le moteur aussi, tourner sept fois vos doigts dans vos mains avant d'agir !

De même, il est assez difficile de placer le palonnier dans l'arbre, vous aurez certainement à utiliser une vis (M2.5x8mm) et la serrer pour assembler correctement les deux éléments.

## 2. Configuration des moteurs
Lorsque vous sortez le moteur de sa boîte, son ID interne est 1. Aussi, avant de le brancher sur le bus de communication, vous aurez à le configurer. Autrement vous aurez des problèmes comme expérimentés dans ce  [topic](https://forum.poppy-project.org/t/dynamixel-first-uses/91/5).

VOus avez trois paramètres à régler :

 1. L'**ID doit correspondre à notre [convention][1]**
 2. La **vitesse de transmission** doit être **réglée sur 1 000 000bps** au lieu de 57142bps
 3. Le  **délai de temps de retour** doit être réglé sur **0 ms** au lieu de 0.5 ms

Pour régler ces paramètres vous pouvez utiliser le [Dynamixel Wizard][2] (windows) ou [Herborist][3] (Unix/Windows).
<a class="attachment" href="http://www.robotis.com/xe/download_en/657775">RoboPlus v1.1.1.0 </a>

Si vous utilisez [une prise USB2AX][4] sous windows, vous aurez à l'installer manuellement en utilisant ce fichier : <a class="attachment" href="https://github.com/Xevel/usb2ax/raw/master/firmware/lufa_usb2ax/USB2AX.inf">USB2AX.inf</a> (2 KB).
Pour plus d'infos sur cette installation, merci de consulter le [guide d'installation][5].


  [1]: https://forum.poppy-project.org/t/assembly-instructions-motor-naming-convention-and-configuration/87
  [2]: http://support.robotis.com/en/software/roboplus/dynamixel_monitor/quickstart/dynamixel_monitor_connection.htm
  [3]: http://poppy-project.github.io/pypot/herborist.html
  [4]: http://www.xevelabs.com/doku.php?id=product:usb2ax:usb2ax
  [5]: http://www.xevelabs.com/doku.php?id=product:usb2ax:quickstart
