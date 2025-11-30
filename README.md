# ufw.miniprojekti


Idempotentti UFW-Konfiguraatio SaltStackilla – Turvallinen Tiimiprojekti. Tässä projektissa konfiguroidaan UFW Saltilla Debian-serverille, avaten vain SSH (22), HTTP (80) ja HTTPS (443). 

Opitte myös, miten mitä tahansa portteja saadaan auki SaltStackilla ja mitä hyötyä siitä voi olla teille työelämässä. 

**Ennen**                   





**Jälkeen** 



Saltin sisällä ajetaan mainitsemat 3 porttia läpi: 

ufw_allow_ssh:   
  ufw.allow:     
    - name: 22/tcp   
    - require_in:      
        - service: ufw_service
 
ufw_allow_http:   
   ufw.allow:     
     - name: 80/tcp   
     - require_in:     
         - service: ufw_service
 
 
ufw_allow_https:   
   ufw.allow:  
     - name: 443/tcp  
     - require_in:      
        - service: ufw_service
