Библиотека `numpy` работает с объектами-массивами, которые способны хранить много значений и быть многомерными. При этом, в отличие от списков, массивы могут хранить только значения одного типа. За счёт этого массивы в `numpy` занимают меньше памяти и работают быстрее, чем списки.

```Python
import numpy as np
```

## **Изменение массива**
### **reshape()**
`reshape()` - принимает кортеж, значения которого задают новые размеры массива по осям, возвращает новый массив. Обратите внимание: при изменении размерности количество элементов в массиве не должно измениться.
```python
import numpy as np 
a = np.zeros((4, 3), dtype="uint8") 
print(a)
a = a.reshape((2, 6)) 
print(a)
```
Если при изменении размерности в функции указать значение -1 по одной или нескольким осям, то значения размерности рассчитаются автоматически.
### **resize()**
`resize()` - меняет размерность исходного массива
```python
import numpy as np
a = np.zeros((4, 3), dtype="uint8")
print(a)
a.resize((2, 2, 3))
print(a)
```

## **Математика**
Для работы с массивами доступны все стандартные арифметические операции, а также тригонометрические, экспоненциальная и другие функции. Выполнение математических операций над массивами происходит поэлементно. Размерность массивов должна совпадать при выполнении этих операций.
### **4 действия**
```python
import numpy as np
a = np.array([9, 8, 7])
b = np.array([1, 2, 3])
print(a + b) #Сложение
print(a - b) #Вычитание
print(a @ b) #Умножение
print(a / b) #Деление
```

### **Вращение**
Матрицы можно транспонировать функцией `transpose()` и поворачивать функцией `rot90()`
При повороте можно указать направление поворота вторым аргументом.
```python
import numpy as np
a = np.arange(1, 13).reshape(4, 3)
print(a.transpose()) #Транспонирование
print(np.rot90(a)) #Поворот влево
print(np.rot90(a, -1)) #Поворот вправо
```

#python #numpy #Основа 