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
![Capture d'écran 2024-12-12 203334](https://github.com/user-attachments/assets/b4f7525a-1996-48a3-a3ea-dfb510d59e9d)  


Montage du snapshot dans `home-snap`  
![Capture d'écran 2024-12-12 203341](https://github.com/user-attachments/assets/d1744c22-d150-488d-a24d-a8bc6ef5f4e7)  


On vérifie que le snapshot contient bien le /home d'origine.  
![Capture d'écran 2024-12-12 203537](https://github.com/user-attachments/assets/b60e4440-278d-44a4-be83-7268c5278000)  

Démontage du dossier /home-snap  
![Capture d'écran 2024-12-12 204150](https://github.com/user-attachments/assets/634d03b6-9da1-4ae2-9b45-5f99fb188614)  


Vérification que /home-snap n'est plus affiché.  
![Capture d'écran 2024-12-12 204208](https://github.com/user-attachments/assets/86f9c9ab-6c37-427c-995e-04c63469cc46)  

Avec lvs, on voit le snapshot à détruire.  
![Capture d'écran 2024-12-12 204503](https://github.com/user-attachments/assets/ed4b4e7f-5749-42b2-acbe-bfc4ba177ae1)  

Suppression du volume logique du snapshot.  
![Capture d'écran 2024-12-12 204732](https://github.com/user-attachments/assets/bd47c35f-1368-4c8c-bc77-67f290f1dc55)


Vérification.  
![Capture d'écran 2024-12-12 204830](https://github.com/user-attachments/assets/e942b62e-934a-4376-92f1-9b9d32db04ae)
![Capture d'écran 2024-12-12 205013](https://github.com/user-attachments/assets/9aad2167-b5ff-4883-8d76-86a28beb25d6)


Et voilà le snapshot a disparu et le `home` n'est plus la source de snapshot !!!  
