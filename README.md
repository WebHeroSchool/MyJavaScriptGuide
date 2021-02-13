# JavaScript Style Guide by Viktorija. :wink:

### 1.Переменные
Переменные должны называться по смыслу, так что можно было понять что это за значение, которое будет храниться в них. В названии переменных можно использовать лишь 2 символа $ и _ , так же можно использовать цифры, но в конце названия переменной. А ещё можно называть пользуясь методом camel case.

**Правельно**

```
let userName = "Vika";
let userAge = " 25";
```

**Не правельно**
```
let imja = "Vika";
let 1Let = "25";
```

### 2.Объявление переменных
Используйте let или const для объявления переменных.

**Правельно**

```
let userName = "Nicoleta";
```

**Не правельно**
```
userName = "Nicoleta";
```

### 3.Точка с запятой
Всегда ставьте точку с запятой в конце выражения.Точки с запятой должны присутствовать после каждого выражения, даже если их, казалось бы, можно пропустить.

Есть языки, в которых точка с запятой необязательна и редко используется. Однако в JavaScript бывают случаи, когда перенос строки не интерпретируется, как точка с запятой, что может привести к ошибкам.

**Правельно**

```
alert("Теперь всё в порядке");

[1, 2].forEach(alert)
```
 В результате получим сообщение «Теперь всё в порядке», следом за которым будут 1 и 2.

**Не правельно**
```
alert("Сейчас будет ошибка")

[1, 2].forEach(alert)
```
Если запустить код, выведется только первый alert, а затем мы получим ошибку!

### 4.Комментарии

Со временем программы становятся всё сложнее и сложнее. Возникает необходимость добавлять комментарии, которые бы описывали, что делает код и почему.

Комментарии могут находиться в любом месте скрипта. Они не влияют на его выполнение, поскольку движок просто игнорирует их.

**Однострочные комментарии начинаются с двойной косой черты //.**

Часть строки после **//** считается комментарием. Такой комментарий может как занимать строку целиком, так и находиться после инструкции.

Как здесь:
```
// Этот комментарий занимает всю строку
alert('Привет');

alert('Мир'); // Этот комментарий следует за инструкцией
```
**Многострочные комментарии начинаются косой чертой со звёздочкой  и заканчиваются звёздочкой с косой чертой.**

Как вот здесь:
```
/* Закомментировали код
alert('Привет');
*/
alert('Мир');
```

### 5.Отступы
Существует два типа отступов:

+ Горизонтальные отступы: два или четыре пробела.

Горизонтальный отступ выполняется с помощью 2 или 4 пробелов, или символа табуляции (клавиша Tab). Какой из них выбрать – это уже на ваше усмотрение. Пробелы больше распространены.

Одно из преимуществ пробелов над табуляцией заключается в том, что пробелы допускают более гибкие конфигурации отступов, чем символ табуляции.

Например, мы можем выровнять аргументы относительно открывающей скобки:
```
show(parameters,
     aligned, // 5 пробелов слева
     one,
     after,
     another
  ) {
  // ...
}
```
+ Вертикальные отступы: пустые строки для разбивки кода на «логические блоки».

Даже одну функцию часто можно разделить на логические блоки. В примере ниже разделены инициализация переменных, основной цикл и возвращаемый результат:

```
function pow(x, n) {
  let result = 1;
  //              <--
  for (let i = 0; i < n; i++) {
    result *= x;
  }
  //              <--
  return result;
}

```
Вставляйте дополнительный перевод строки туда, где это сделает код более читаемым. Не должно быть более 9 строк кода подряд без вертикального отступа.