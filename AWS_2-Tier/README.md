## VPC μμ±
![image](https://user-images.githubusercontent.com/117608997/216535436-c901f042-fe03-4325-8774-702eb021f1d5.png)


### π‘ VPC
- Public Subnet : 2κ°
- Web Subnet : 2κ°
- DB Subnet : 2κ°
- EFS Subnet : 2κ°
- NAT Gateway : 2κ°
</br>

### π‘ μλΈλ· μΆκ° μμ±
- a μμ­ Subnet : 10.0.4.0/24
- c μμ­ Subnet : 10.0.44.0/24
</br>
<hr/>

## Security Group μμ±
![image](https://user-images.githubusercontent.com/117608997/216542940-9eef744a-5152-4b99-b5ad-27bc36127bf6.png)

### π‘ Security Group
- HTTP : Web Security Group
- MySQL : DB Security Group
- EFS : EFS Security Group
</br>
<hr/>

## RDS μμ±
![image](https://user-images.githubusercontent.com/117608997/216536797-4bf0b531-099e-4b9b-9d3e-9cb9f4e2bce0.png)

### π‘ DB Subnet κ°μ©μμ­ μΆκ°
- Private 2a : 10.0.3.0/24
- Private 2c : 10.0.33.0/24
</br>
<hr/>

## EC2 μμ±
![image](https://user-images.githubusercontent.com/117608997/216537101-cc064bbf-7980-4581-b379-a58460b42a59.png)

### π‘ EC2 μΈμ€ν΄μ€ Public 2cμ μμ±
</br>
<hr/>

## EFS μμ±
![image](https://user-images.githubusercontent.com/117608997/216538453-0aab5944-caf7-4b91-a8ff-2451d5e8df2b.png)

### π‘ EFS μμ± ν μκ΅¬ λ§μ΄νΈ μ€μ 
</br>
<hr/>

## Load Balancer
![image](https://user-images.githubusercontent.com/117608997/216538813-74fb2c19-214e-4d61-b967-7d5ad354d2a5.png)

### π‘ Load Balancer Target Group ν Load Balancer μμ±
</br>
<hr/>

![TargetGroup](https://user-images.githubusercontent.com/117608997/215333986-fe91473e-c282-4a32-a52a-c53386696eda.jpg)
### π‘ Target Group μμ±
</br>
<hr/>

![Load Balancer μμ±](https://user-images.githubusercontent.com/117608997/215334100-15039965-990e-47f2-a46b-f7eb45223ff6.jpg)
### π‘ Load Balancer μμ±
**< κΈ°λ³Έκ΅¬μ± >**
- AteamLoadBalancer
- μΈν°λ· κ²½κ³
- IPv4

**< λ³΄μκ·Έλ£Ή >**
- Web Security Group

**< λ€νΈμν¬ λ§€ν >**
- VPC : A team- (public 2a/ public 2c)

**< λ¦¬μ€λ λ° λΌμ°ν >**
- HTTP : 80 (default)
</br>
<hr/>

## Auto Scaling
![image](https://user-images.githubusercontent.com/117608997/216540912-9b53d90d-fb8b-4185-85ee-9c6189dfe530.png)

### π‘ Auto Scaling AMI μ΄λ―Έμ§λ‘ μμ κ·Έλ£Ή μμ± ν Auto Scaling μμ±
</br>
<hr/>

![AMI](https://user-images.githubusercontent.com/117608997/215333749-f880d18b-4983-42e7-be4a-d1913818107f.jpg)
### π‘ Auto Scaling AMI μ΄λ―Έμ§ μμ±
</br>
<hr/>

![μμκ΅¬μ±](https://user-images.githubusercontent.com/117608997/215333757-4674a58f-dce4-46f4-b6e8-deda93a9cd87.jpg)
### π‘ Auto Scaling μμκ΅¬μ± μμ± 
**< μμ κ΅¬μ± >**
- AMI μ΄λ―Έμ§ μ ν
- Load Test νμΈμ μν΄ λͺ¨λν°λ§ νμ±ν
- μΈμ€ν΄μ€ μ ν : t2.micro
- λ³΄μκ·Έλ£Ή : SSH, HTTP Security Group
- ν€ νμ΄ μ¬μ©
</br>
<hr/>

![AutoScaling  μμ±](https://user-images.githubusercontent.com/117608997/215333774-efba4114-10da-4afd-a857-e95e0df1338e.jpg)
### π‘ Auto Scaling μμ± 
**< Auto Scaling μμ± κ΅¬μ±>**
</br>
**- 1λ¨κ³**
  - μμ±ν μμ κ΅¬μ± μ ν

**- 2λ¨κ³**
  - Auto Scaling λ€νΈμν¬ μ€μ 

**- 3λ¨κ³**
  - κ³ κΈ μ΅μ κ΅¬μ±

**- 4λ¨κ³**
  - κ·Έλ£Ή ν¬κΈ° λ° ν¬κΈ° μ‘°μ  μ μ± κ΅¬μ±

**- 5,6λ¨κ³**
  - μλ¦Ό/νκ·Έ μΆκ° μ€μ  x
</br>
<hr/>

![Auto Scaling νμΈ](https://user-images.githubusercontent.com/117608997/215333831-dca840b4-f27c-480d-bb3c-2de1feeaf6ed.jpg)
### π‘ Auto ScalingμΌλ‘ μΈμ€ν΄μ€ μ΅μ 2κ° μ¦κ° νμΈ
</br>
<hr/>

![κ°μ©μμ­ λ³κ²½ νμΈ](https://user-images.githubusercontent.com/117608997/215333845-d470ca85-630c-48ec-9f15-b37d751fbb11.jpg)
### π‘ λ‘λλ°Έλ°μ DNSλ‘ μ μ β κ°μ©μμ­ λ³κ²½ νμΈ
</br>
<hr/>

![μΈμ€ν΄μ€ μ¦κ°](https://user-images.githubusercontent.com/117608997/215334420-7988ff65-8dfc-4466-ac49-34497d177e1a.jpg)
### π‘ λΆν λΆμ° λ° Auto Scaling νμΈ
</br>
<hr/>

## S3
![image](https://user-images.githubusercontent.com/117608997/216542241-f31814a2-ca2b-4f41-8c11-fefb4bc88554.png)

</br>

![S3 static νΈμ§](https://user-images.githubusercontent.com/117608997/215333892-e543f8a2-97b0-45d3-aadc-f8701d158420.jpg)
### π‘ S3 λ²ν· μμ± ν νμΌ μλ‘λ λ° νΌλΈλ¦­ μ€μ , Cloudfrontμμ EC2 Load Balancer λ°°ν¬
</br>

![S3](https://user-images.githubusercontent.com/117608997/215331385-59945152-4262-484e-88b2-b900cf5e6357.jpg)
### π‘ Static Web Site νμΌ S3μ μΆκ°
</br>
<hr/>

## Cloud Front λ° Failover
![CloudFront](https://user-images.githubusercontent.com/117608997/215331915-aa259c14-3ef2-49e6-a6aa-93d290e7b517.jpg)

### π‘ μμ±ν λλ©μΈμ cloudfrontμ λμ²΄λλ©μΈ μΆκ° ν μ μ
</br><hr/>

![Failover_normal](https://user-images.githubusercontent.com/117608997/215331395-429a806c-0ad3-446f-b140-5b9feb687ccf.jpg)
### π‘ μ μ μ μμ Web νμΈ
</br><hr/>

![Failover_static](https://user-images.githubusercontent.com/117608997/215331422-ad9f9d25-1c3d-4086-b0b3-530a5d242bb8.jpg)
### π‘ μ₯μ  λ°μ ν λλ©μΈ μ μ μ Statice Web μ μ νμΈ
</br><hr/>
