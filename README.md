Выполнения проекта JvmComprehension:



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
    }}

//1 в стеке добавляются примитив int i = 1

//2 в стеке добавляется Object о в кучу = 0

//3 в стеке ссылка добавлена Integer ii = 2

//4 в стеке o-связывается с кучей,i-связывается с кучей,ii-связывается с кучей

//5 в стеке uselessVar = 700 связывается с кучей Integer

//6 создается фрейм который получает ссылку на i, и ссылки на обьекты o, ii получаем из данных кучи.

//7 System.out.println("finished") выводит в консоль строку

Загрузка классов JvmComprehension с помощью ClassLoading

Работает подсистема загрузчиков класса ClassLoader

Возвращается объект класса и передается  Bootstrap

В памяти программы происходит множество процессов с помощью компилятора и сборщика мусора

Код выполняется построчно и компилируются в машинный код
Сборщик мусора находит неиспользуемые объекты и удаляет это освобождает память

