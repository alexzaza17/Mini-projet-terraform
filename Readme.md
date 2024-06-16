# Fankem

## Alex Junior

### Eazytraining 18th DevOps Bootcamp

#### Period: march-april-may

Application

Il est question ici pour nous de mettre en place un code terraform qui nous permettra de provisionner notre console aws: 
Notre VM doit fonctionner le AMI ubuntu bionic, cette image s attachera a notre Elastic Blok Store et Elastic IP et nous allons variabilises le taille et le tag
Nous creer les resources ebs et une EIP qui devra s atteche a l EIP, mais ceci n est pas possibe raison pour laquelle nous allons attache l ec2 a la security group, puisque l ec2 pourra attacher l eip 

Plan  de travail 
Nous avons cree le fichier module qui contient nous quatre differents modules a savoir:
- ec2 qui comporte en son sein: le fichier main, varaiable et le output
- ebs qui comporte en son sein: le fichier main, varaiable et le output
- eip qui comporte en son sein: le fichier main, varaiable et le output
- sg qui comporte en son sein: le fichier main, varaiable et le output
Ensuite nous avons cree le fichier main.tf qui contient notre secret key et access key et aussi c est dans ce fichier que nous vons fait l attachement des differents modules
En fin il y a le fichier devops-Alexzaza qui contient notre cle pem

Elaboration du plan de travail
Nous avons d abord cree a resource ebs qui est Elastic Block Store il est considere comme le disque C du personnel computer et nous avons variabile ce volume et surtout precise la region dans laquelle ce volume se trouve qui doit etre la meme region que celle de l ec2
Nous avons cree le ec2 qui permet de creer l AMI et le recupere de facon dynamique en utilisation les data et celui-ci  est attache au ebs, au eip et au sg. l attachement des differents modules se fait par a sortie(output) de chacun de ses modues et se fait dans le fihier main.tf
Noous avons cree le eip 
Nous avons cree la security group et defini les differents ports auxquels la security sera connnecte
En fin nous avons installe nginx et stocke l adresse ip

![Aws1](https://github.com/alexzaza17/Mini-projet-terraform/assets/159175882/51afd0a3-39f2-4703-b36a-05bb93177c13)


![Aws2](https://github.com/alexzaza17/Mini-projet-terraform/assets/159175882/935b47df-a6b3-4da8-9bba-efa278ee340d)


![VW-Aws](https://github.com/alexzaza17/Mini-projet-terraform/assets/159175882/f0a84169-ac2e-4eef-b1f2-8cb8a6b7965d)


![Server nginx](https://github.com/alexzaza17/Mini-projet-terraform/assets/159175882/c94fd223-4273-4868-bbc2-eaf23f92bc0a)
