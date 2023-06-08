- 👋 Hi, I’m @Merveuyu
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Merveuyu/Merveuyu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import random

def zar_atma_oyunu():
    oyuncu1_skor = 0
    oyuncu2_skor = 0

    def boyama(resim, skor):
        if skor == 7:
            return resim.replace(" 7 ", " *7* ")
        elif skor == 10:
            return resim.replace(" 10 ", " *10* ")
        else:
            return resim

    while True:
        # Oyuncu 1'in sırası
        input("Oyuncu 1, zar atmak için bir tuşa basın.")
        zar1_1 = random.randint(1, 6)
        zar1_2 = random.randint(1, 6)
        toplam1 = zar1_1 + zar1_2
        resim1 = f"  {zar1_1}  +  {zar1_2}  =  {toplam1}  "

        oyuncu1_skor += toplam1
        print(boyama(resim1, toplam1))

        # Oyuncu 2'nin sırası
        input("Oyuncu 2, zar atmak için bir tuşa basın.")
        zar2_1 = random.randint(1, 6)
        zar2_2 = random.randint(1, 6)
        toplam2 = zar2_1 + zar2_2
        resim2 = f"  {zar2_1}  +  {zar2_2}  =  {toplam2}  "

        oyuncu2_skor += toplam2
        print(boyama(resim2, toplam2))

        print("Oyuncu 1 Skoru:", oyuncu1_skor)
        print("Oyuncu 2 Skoru:", oyuncu2_skor)

        if oyuncu1_skor >= 20 or oyuncu2_skor >= 20:
            break

    if oyuncu1_skor > oyuncu2_skor:
        print("Oyuncu 1 Kazandı!")
    elif oyuncu2_skor > oyuncu1_skor:
        print("Oyuncu 2 Kazandı!")
    else:
        print("Berabere!")
