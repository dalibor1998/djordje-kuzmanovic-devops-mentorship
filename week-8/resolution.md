### Kreiran AMI image od instance "ec2-djordje-kuzmanovic-web-server" naizva: "ami-djordje-kuzmanovic-web-server"

![AMI](https://i.imgur.com/1SkowuE.png)


### Kreiran Application Load Balancer naziva "alb-web-servers", povezan sa Target Group "tg-web-servers"
![ALB](https://i.imgur.com/DnCxPbh.png)


### Kreirana Auto Scaling grupa:
- minimalno 2, maksimalno 4 instance,
- tip instance t2.micro koristiti alb-web-servers load balancer
![ASG](https://i.imgur.com/kxL30y9.png)

- CloudWatch alarm CPU > 18% = deploy 1 unit
- CloudWatch ok CPU < 18% = terminate 1 unit
![ASG](https://i.imgur.com/okugvft.png)


### Security grupe ažurirane da koriste minimalno portova
![SG-EC2](https://i.imgur.com/0L6IL1J.png)
![SG-ALB](https://i.imgur.com/OK4F4lt.png)

### Kreiran dijagram arhitekture korištene za ovaj task

![Architecture](https://i.imgur.com/LBPBTVD.png)


### Dijagram se može preuzeti na sljedećem linku:
[ASG architecture by Djordje Kuzmanovic](https://drive.google.com/file/d/1ZoeGukmiJpcHITzy5doEUoUAf9sU-Mlb/view?usp=sharing)

### Link prema Load Balancer DNS name-u:
[DevOps Mentorship Program app](http://alb-web-servers-813418267.eu-central-1.elb.amazonaws.com)

