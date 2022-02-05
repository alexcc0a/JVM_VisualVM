
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