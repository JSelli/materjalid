

Tsüklid
================

+------------------------------------------------------+----------------------------------------------------------+
| Python                                               | Java                                                     |
+======================================================+==========================================================+
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     for i in range(10):                              |     for (int i = 0; i < 10; i++) {                       |
|         print(i)                                     |         System.out.println(i);                           |
|                                                      |     }                                                    |
|                                                      |                                                          |
|                                                      | Või kasutades *stream*'i:                                |
|                                                      |                                                          |
|                                                      | .. code-block:: java                                     |
|                                                      |                                                          |
|                                                      |     IntStream.range(0, 10).forEach(System.out::println); |
|                                                      |                                                          |
|                                                      |                                                          |
+------------------------------------------------------+----------------------------------------------------------+
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     i = 0                                            |     int i = 0;                                           |
|     while i < 10:                                    |     while (i < 10) {                                     |
|         print(i)                                     |         System.out.println(i++);                         |
|         i += 1                                       |         // i++ -> prints out the current value           |
|                                                      |         // of i, then increments it by 1                 |
|                                                      |     }                                                    |
|                                                      |                                                          |
+------------------------------------------------------+----------------------------------------------------------+
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     lst = [1, 2, 3]                                  |     List<Integer> list = new ArrayList<>();              |
|     for x in lst:                                    |     list.add(1); list.add(2); list.add(3);               |
|         print(x)                                     |     //List<Integer> list = new ArrayList<>(              |
|                                                      |     //    Arrays.asList(new Integer[] {1, 2, 3}));       |
|                                                      |     for (Integer x : list) {                             |
|                                                      |         System.out.println(x);                           |
|                                                      |     }                                                    |
|                                                      |                                                          |
|                                                      | Või kasutades *stream*'i:                                |
|                                                      |                                                          |
|                                                      | .. code-block:: java                                     |
|                                                      |                                                          |
|                                                      |     List<Integer> list = new ArrayList<>(                |
|                                                      |             Arrays.asList(new Integer[] {1, 2, 3})       |
|                                                      |     );                                                   |
|                                                      |     list.stream().forEach(System.out::println);          |
|                                                      |                                                          |
+------------------------------------------------------+----------------------------------------------------------+
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     for x in range(10, 0, -2):                       |     for (int i = 10; i > 0; i -= 2) {                    |
|         print(x)                                     |         System.out.println(i);                           |
|                                                      |     }                                                    |
|                                                      |                                                          |
+------------------------------------------------------+----------------------------------------------------------+
| Paarisarvude summa                                                                                              |
+------------------------------------------------------+----------------------------------------------------------+
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     even_sum = 0                                     |     int evenSum = 0;                                     |
|     for x in range(10):                              |     for (int i = 0; i < 10; i++) {                       |
|         if x % 2 == 0: even_sum += x                 |         if (i % 2 == 0) evenSum += i;                    |
|                                                      |     }                                                    |
|     print(even_sum)                                  |     System.out.println(evenSum);                         |
|                                                      |                                                          |
| Või kasutades lambdat:                               | Või kasutades *stream*'i/lambdat:                        |
|                                                      |                                                          |
| .. code-block:: python                               | .. code-block:: java                                     |
|                                                      |                                                          |
|     print(sum([x for x in range(10) if x % 2 == 0])) |     System.out.println(                                  |
|                                                      |             IntStream.range(0, 10)                       |
|                                                      |             .filter(x -> x % 2 == 0)                     |
|                                                      |             .sum()                                       |
|                                                      |     );                                                   |
|                                                      |                                                          |
+------------------------------------------------------+----------------------------------------------------------+


Loe tsüklite kohta siit: :doc:`../Loop`.

.. generated using "python3 rst_table.py loop_helper.txt loop.rst"