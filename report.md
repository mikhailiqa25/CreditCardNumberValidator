# Отчёт о тестировании CreditCardNumberValidator

## Краткое описание

04.12.2021 - 04.12.2021 было проведено санитарное тестирование кода CreditCardNumberValidator.

На тестирование затрачено: 10 мин

В результате тестирования выявлен дефект при работе с картами American Express
![American fail](https://user-images.githubusercontent.com/94222135/144705456-ded82e12-8889-4c84-83a3-2883cb845883.png)

- При подстановки валидного номера карт VISA, MasterCard и Discover результат положительный:
на примере Visa
![VISA](https://user-images.githubusercontent.com/94222135/144705212-66f0e7d9-a7c2-4b24-b0ae-fbd351c96d75.png)

- При подстановки невалидного номера карт VISA, MasterCard и Discover результат отрицательный:
на примере Visa
![VISA FAIL](https://user-images.githubusercontent.com/94222135/144705234-eaed5f33-9446-4b74-bf7f-943fc384ed7b.png)

посему можно сделать вывод что данный кусок кода "рабочий и способен определить валидность введенных данных таких карт как VISA, MasterCard и Discover. 

## Описание процесса тестирования

В качестве тестовых данных использовались генерируемые данные несуществующих карт [<вот с такого сайта например>](https://www.getcreditcardnumbers.com/):
* Visa 4485142355169158 данные приняты
* Mastercard 5221389339737941 данные приняты
* Discover 6011436366478774 данные приняты
* American Express 372665465992444 данные приняты

Тестирование производилось в следующем окружении:

- Debian GNU/Linux 10 (buster) 4.19.208-1 (2021-09-29) (x86_64)
- версия Java azul-11.0.13
- IntelliJ IDEA 2021.3 (Community Edition)
