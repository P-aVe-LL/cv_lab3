# cv_lab3
# Теория
В соответствии с заданием лабораторной работы были выбраны 3 архитектуры:
1. ResNet50 - архитектура, использующая ResBlock [1].
2. VGG16 - 16 слоев, большие свертки представляются как комбинации сверток 3x3 [3].
3. Inception V3 - 42 слоя, вместо сверток NxN используются комбинации сверткок Nx1 и 1xN  [2][3].

# Описание разработанной системы
Была разработана программа на языке Python, которая реализует предсказание класса на картинке для моделей Inception V3, ResNet50 и VGG16. Для них же высчитываются метрики top1 и top5, а также среднее время распознавания картинки и количество используемой памяти.

# Результаты работы программы
Результат предсказания картинки  с истиным классом 'armadillo':  
  ('n02454379', 'armadillo', 0.9995795),  
  ('n01688243', 'frilled_lizard', 5.9008882e-05),  
  ('n13133613', 'ear', 4.3292705e-05),  
  ('n03980874', 'poncho', 4.236992e-05),  
  ('n01797886', 'ruffed_grouse', 2.5804777e-05)

# Результаты сравнения моделей
| Model         | Top1   | Top5  | Memory usage, Mb | Time, s
|---------------|:------:| -----:|:----------------:|:------:|
| ResNet50      | 0.68   |  0.96 |  2378            | 1.23
| VGG16         | 0.64   |  0.96 |  2323            | 0.67
| Inception V3  | 0.84   |  1.0  |  2264            | 0.92

# Выводы по работе
В результате работы было выяснено, что Inception V3 обладает самой высокой точностью, тратит меньше всего памяти и занимает второе место по скорости работы.

# Использованные источники
[1] https://towardsdatascience.com/residual-blocks-building-blocks-of-resnet-fd90ca15d6ec  
[2] https://dev-gang.ru/article/-luczshih-predvaritelno-podgotovlennyh-modeli-dlja-klassifikacii-izobrazhenii-s-pomosczu-koda-python-00gddb9o3g/  
[3] https://logic.pdmi.ras.ru/~sergey/teaching/mlspsu18/28-cnn2.pdf
