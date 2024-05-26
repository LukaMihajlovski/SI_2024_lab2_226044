# SI_2024_lab2_226044
1.Luka Mihajlovski 226044
2.![image](https://github.com/LukaMihajlovski/SI_2024_lab2_226044/assets/167027515/46f8aa2c-8fa7-40b4-9df4-01963d940ecb)

3.CIKLOMATSKATA VREDNOST SE PRESMETUVA: brojot na rebra - brojot na teminja + 2 = 42 - 34 + 2 = 10

4.Има 8 тестови:

1. Вредноста на параметарот allItems е null, фрли RuntimeException.
   - allItems = null
   
3. allItems содржи елемент нема валиден баркод, па се очекува програмата да фрли RuntimeException.
   - allItems = [["twerk ticket", "s690", 0, 0.0]]
4. allItems има елемент каде баркодот е еднаков на null, па се очекува програмата да фрли RuntimeException.
   - allItems = [["domat", null, 2, 0.3]]
5. allItems му фали име на продукт, па се очекува програмата да му го додели името "unknown".
   - allItems = [["", 0692, 2, 0.3]]
6. Продуктите немаат попуст, а збирот на цени е помал или еднаков на payment.
   - allItems = [["domat", "0692", 68, 0], ["head", "2303", 69, 0]] и payment = 500
7. Payment е помал од цената која треба да се плати, и немаат попуст.
   - allItems = [["domat", "2108", 2, 0], ["kolbasi", "3105", 1, 0]] и payment = 1
8. Исто како барањето под 5. само има попуст.
   - allItems = [["domat", "0692", 68, 0.69], ["head", "2303", 69, 0.31]] и payment = 500
9. Исто како барањето под 6. само има попуст.
   - allItems = [["domat", "2108", 2, 0.31], ["kolbasi", "3105", 1, 0.69]] и payment = 1
Критериумот Every Branch е задоволен.

5.`if (item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0')`
има 4 такви тест случаи:

1. Цена е помала од 300.
   - item = ["kolbasi", "2445",30, 0.1]
2. Цена е поголема од 300, нема попуст.
   - item = ["kolbasi", "2445", 301, 0]
3. Цена е поголема од 300,има попуст, но баркотдот почнува со 0.
   - item = ["kolbasi", "0690", 301, 0.1]
4. Цена е поголема од 300,има попуст, баркодот е ок.
   - item = ["kolbasi", "2445", 301, 0.1 ]
