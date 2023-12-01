# SureliSifreUret
import random 
import time

def sifre_olustur(): 
    sifre = ""
    for i in range(6): 
        sifre = sifre + str(random.randint(0,9))
    return sifre 

def sifre_sor(sifre): 
    cevap = input("Lütfen yeni şifre alabilmek için eski şifrenizi giriniz: ") 
    if cevap == sifre:
        print("Doğru cevap!") 
    else: 
        print("Yanlış cevap!") 
        cevap = input("Lütfen yeni şifre alabilmek için eski şifrenizi giriniz: ") 
while True: 
    sifre = sifre_olustur() 
    print("Şifreniz:", sifre) 
    print("Şifrenizin 60 sn kullanım hakkı vardır...")
    time.sleep(6) 
    sifre_sor(sifre) 

