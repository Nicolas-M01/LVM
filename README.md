# LVM

J'ajoute un Disque de 25Go dans VirtualBox.  
`lsblk` pour le voir dans le système "sdb".  
![Capture d'écran 2024-12-12 194021](https://github.com/user-attachments/assets/9f79fb65-0a54-4053-822b-f0b46d989475)  

Création du volume physique.  
![Capture d'écran 2024-12-12 201600](https://github.com/user-attachments/assets/8f980eec-bdfe-4193-bd28-b51dd7d1bdb8)  

Ajout au groupe de volume.  
![Capture d'écran 2024-12-12 201918](https://github.com/user-attachments/assets/c1acc163-b6e2-4396-ae01-d13d7a3b83e3)  

Le volume a bien doublé.  
![Capture d'écran 2024-12-12 202028](https://github.com/user-attachments/assets/aab962d7-7712-42e9-aabc-24ea9fb27f81)  

Création Snapshot.  
![Capture d'écran 2024-12-12 202720](https://github.com/user-attachments/assets/df1573e0-ae5b-4945-92c3-1443d90ec827)  

Création du dossier `home-snap`  
![Capture d'écran 2024-12-12 202720](https://github.com/user-attachments/assets/ecdf0f26-eae1-405c-814a-3d0d3acc8997)  

Montage du snapshot dans `home-snap`  
![Capture d'écran 2024-12-12 203334](https://github.com/user-attachments/assets/c5f60487-a39c-4bad-94d0-a85684f3d748)  

On vérifie que le snapshot contient bien le /home d'origine.  
![Capture d'écran 2024-12-12 203537](https://github.com/user-attachments/assets/b60e4440-278d-44a4-be83-7268c5278000)


