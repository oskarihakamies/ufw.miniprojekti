# Idempotentti UFW-Konfiguraatio SaltStackilla - Turvallinen Tiimiprojekti

*Tekijät: Oskari Häkämies ja Joonas Janttonen*

Tässä projektissa konfiguroidaan UFW Saltilla Debian-serverille, avaten vain SSH (22), HTTP (80) ja HTTPS (443). Opitte myös, miten mitä tahansa portteja saadaan auki SaltStackilla ja mitä hyötyä siitä voi olla teille työelämässä. 

**Ennen**                   

<img width="458" height="74" alt="image" src="https://github.com/user-attachments/assets/d5594d64-92d4-42f8-9661-f069d36a9a3a" />




**Jälkeen** 

<img width="561" height="211" alt="image" src="https://github.com/user-attachments/assets/ad8c7d12-7ffe-447f-97d3-6fdba2020e1e" />


Saltin sisällä ajetaan mainitsemat 3 porttia läpi: 

ufw_allow_ssh:   
  ufw.allow:     
    - name: 22/tcp   

 
ufw_allow_http:   
   ufw.allow:     
     - name: 80/tcp   

 
 
ufw_allow_https:   
   ufw.allow:  
     - name: 443/tcp  
   
