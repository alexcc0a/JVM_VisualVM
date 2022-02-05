Домашнее задание для Netology.ru для курса Java Developer   

Описание и инструкция к выполнению [здесь](https://github.com/netology-code/jd-homeworks/tree/master/jvm/README.md)

public class JvmComprehension {

    public static void main(String[] args) {
        int i = 1;                      // 1
        Object o = new Object();        // 2
        Integer ii = 2;                 // 3
        printAll(o, i, ii);             // 4
        System.out.println("finished"); // 7
    }

    private static void printAll(Object o, int i, Integer ii) {
        Integer uselessVar = 700;                   // 5
        System.out.println(o.toString() + i + ii);  // 6
    }
}

1. Переменная, значение которой находится в рамках стэка.
2. Создаётся объект в "куче", ссылка на этот объект присваевается в переменную "o".
3. Целочисленный тип данных со значением 2, во фрейм main добавляется переменная ii (ссылка на этот объект).
4. В стеке JvmComprehension создаётся фрейм метода printAll
5. В куче создаётся новый объект Integer, содержащий int со значением 700, во фрейм printAll добавляется переменная uselessVar.
6. В куче создаётся новый объект типа String, во фрейме printAll создаётся переменная (пусть arg) с ссылкой на этот объект, в стеке Object создаётся фрейм метода toString, в куче создаётся новый объект типа String.
7.  В куче создаётся объект типа String, хранящий переданную строку "finished" (вывод в консоль).


<img width="705" alt="Снимок экрана 2022-02-05 в 13 28 54" src="https://user-images.githubusercontent.com/94784081/152636515-2b99bba0-e624-461f-8633-b96ad8e4f491.png">
<img width="1440" alt="Снимок экрана 2022-02-05 в 13 05 10" src="https://user-images.githubusercontent.com/94784081/152636517-13b1322f-1e06-4e55-96ec-d751bffb0895.png">
<img width="465" alt="Снимок экрана 2022-02-05 в 13 41 02" src="https://user-images.githubusercontent.com/94784081/152636522-f708324c-bb61-4fd3-8cd7-c6c5d22e4a6b.png">
