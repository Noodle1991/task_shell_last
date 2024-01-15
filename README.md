#1

Суммирование

Напишите программу, которая находит суммирование каждого числа от 1 до num. Число всегда 
будет целым положительным числом, большим 0.

Например:

sum(2) -> 3

1 + 2

sum(8) -> 36

1 + 2 + 3 + 4 + 5 + 6 + 7 + 8

#2

Возьмите 2 строки s1 и s2, включающие только буквы от a до z.

Возвращает новую отсортированную строку, максимально длинную, содержащую различные буквы 
- каждая из которых берется только один раз - исходящие из s1 или s2.

a = "xyaabbbccccdefww"

b = "xxxxyyyyabklmopq"

longest(a, b) -> "abcdefklmopqwxy"

a = "abcdefghijklmnopqrstuvwxyz"

longest(a, a) -> "abcdefghijklmnopqrstuvwxyz"

#3

Джон пригласил друзей. Его список:

s = 
"Ann:Russel;John:Gates;Paul:Wahl;Alex:Tolkien;Ann:Bell;Lewis:Kern;Sarah:Rudd;Sydney:Korn;Madison:Meta";

Нужно написать программу, которая переводит эту строку в верхний регистр и сортирует ее 
в алфавитном порядке по фамилии.

Если фамилии совпадают, отсортируйте их по имени. Фамилия и имя гостя вводятся в 
результате в скобках через запятую.

Таким образом, результатом будет:

"(BELL, ANN)(GATES, JOHN)(KERN, LEWIS)(KORN, SYDNEY)(META, MADISON)(RUDD, SARAH)(RUSSEL, 
ANN)(TOLKIEN, ALEX)(WAHL, PAUL)"

Может случиться так, что в двух разных семьях с одинаковой фамилией два человека также 
имеют одинаковое имя.


ЗАДАЧА 1
```bash
echo "Введите число:"
read num

sum=0
for (( i=1; i<=$num; i++ ))
do
  sum=$((sum + i))
done

echo "Сумма чисел от 1 до $num: $sum"
```

ЗАДАЧА 2
```bash
s1="xyaabbbccccdefww"
s2="xxxxyyyyabklmopq"

result=$(echo -e "$s1\n$s2" | grep -o . | sort -u | tr -d '\n')
echo "Результат: $result"
```

ЗАДАЧА 3
```bash
T^T
```


ПОЯСНЕНИЕ:
grep -o -  Выводит только совпадения, а не целые строки. (HELLO и HELLO,WORLD! -> HELLO)
sort -u - "unique",уникальный - Оставляет только уникальные строки после сортировк
tr -d - delete - Удаляет указанные символы
grep -o . - тоже самое,что и grep -o, но точка - флаг для одиночных символов
