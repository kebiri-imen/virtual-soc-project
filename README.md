# virtual-soc-project
This project presents the design and implementation of a Virtual Security Operations Center (SOC) aimed at detecting, analyzing, and responding to cybersecurity threats in real time. The objective is to simulate a real-world SOC environment and demonstrate practical skills in threat detection, incident response, and security automation.
# architecture physique 
1)réseau d’accès (DMZ / “edge”)
On voit deux zones réseau distinctes :

DMZ (haut gauche)
Elle contient des services d’infrastructure :
DHCP (affectation automatique des IP)
DNS (résolution de noms)
Les équipements de cette DMZ sont raccordés à un équipement réseau central (routeur/firewall / appliance) indiqué sous la zone.
Une plage réseau est annotée :
192.168.6.0 (réseau associé à la DMZ/zone d’edge)
LAN (bas gauche)
C’est le réseau “interne” où se trouvent des postes clients.
Les postes du LAN se branchent à un autre équipement réseau central (switch/routeur ou pare-feu interne selon le contexte).
Une plage réseau est annotée :
192.168.6.0 (même étiquette de réseau sur le schéma pour la zone LAN)
2) Liaison vers Internet/WAN
Une ligne part de l’équipement central vers la zone WAN (icône “cloud”).
C’est la sortie vers l’extérieur (internet) ou vers un flux externe entrant/sortant selon l’usage du SOC.
3) Passage vers le SOC (centre/droite)
Le schéma montre ensuite un équipement “cœur” (notamment marqué pf/pare-feu ou appliance) qui relie le segment d’edge/WAN à la zone de supervision.
La zone SOC correspond à l’environnement de collecte/analyse et supervision.
Réseau interne du SOC
Dans le SOC, on voit une annotation :
192.168.6.0 en bas (réseau interne utilisé dans la zone SOC)
4) Dans le SOC : outils de supervision / collecte / analyse
Le SOC contient plusieurs hôtes/serveurs (postes représentés en haut/bas) connectés entre eux via un backbone réseau.

On distingue plusieurs plateformes/outils :

Suricata : moteur IDS/IPS (détection réseau).
Zabbix : supervision/monitoring (état des services, métriques, alertes).
n8n : automatisation workflows (enchaînement de tâches, réponses, intégrations).
MISP : gestion de Threat Intelligence (IOC, TTP, enrichissements).
TheHive : gestion d’incidents/analyses (corrélation et investigation).
Cortex : analyse/enrichissement (playbooks analytiques).
Un petit pictogramme type “MISP worker / automation” (selon la représentation) s
<img width="845" height="590" alt="Image" src="https://github.com/user-attachments/assets/fbd0f1ff-232b-4188-9388-251d1c3869b4" />









uggère le
