# Прогнозирование мощности кондиционера по заданным параметрам

## Описание

Модель использует правила нечеткой логики для оценки необходимой мощности кондиционера при различных условиях. Она учитывает следующие параметры:

- **Температура**: Диапазон от 0°C до 40°C, разделен на три категории: холодная, комфортная и жаркая.
- **Влажность**: Диапазон от 0% до 100%, разделен на три категории: сухая, нормальная и влажная.
- **Количество людей**: Диапазон от 0 до 10, разделен на три категории: мало, умеренно и многолюдно.

Выходной параметр модели — это оценка мощности в процентах, в пределах от 0% до 100%, которая указывает на энергозатраты кондиционера при заданных условиях.

## Установка

Для запуска кода необходимо установить следующие библиотеки Python:

- **NumPy**: Для численных вычислений.
- **SciKit-Fuzzy**: Для вычислений с использованием нечеткой логики.
- **Matplotlib**: Для построения 3D-графиков.

Для установки зависимостей выполните команду:

```bash
pip install numpy scikit-fuzzy matplotlib
```

## Как использовать

### Входные данные
Модель принимает три входных параметра — температуру, влажность и количество людей.

- **Температура** (от 0°C до 40°C), категория:
  - Холодная: 0-15°C
  - Комфортная: 15-30°C
  - Жаркая: 30-40°C

- **Влажность** (от 0% до 100%), категория:
  - Сухая: 0-40%
  - Нормальная: 40-80%
  - Влажная: 80-100%

- **Количество людей** (от 0 до 10), категория:
  - Мало: 0-4 человека
  - Умеренно: 4-8 человек
  - Многолюдно: 8-10 человек

### Запуск кода
Программа применяет правила нечеткой логики к этим входам, чтобы предсказать требуемую мощность кондиционера.

### Пример входных данных:
```python
temp_level = 'comfortable'
humidity_level = 'normal'
people_level = 'few'

power_output = apply_rules(temp_level, humidity_level, people_level)
print(f'Выходная мощность: {power_output}')
```

### Выход:
Выходом будет оценка потребляемой мощности в зависимости от условий, например:

```yaml
Выходная мощность: 35
```

## Ключевые особенности

- **Нечеткая логика**: Модель использует нечеткую логику для имитации поведения кондиционера на основе входных данных, что делает прогноз более гибким и реалистичным.
- **3D визуализация**: Три 3D-графика показывают зависимость между температурой, влажностью и количеством людей с предсказанным потреблением энергии.

## Пример графиков

Следующие 3D-графики визуализируют зависимость между входными параметрами и прогнозируемым потреблением энергии:

1. Температура, Влажность и Мощность
2. Температура, Количество людей и Мощность
3. Влажность, Количество людей и Мощность

Эти графики строятся с использованием Matplotlib и помогают визуализировать, как меняется потребление энергии в зависимости от различных условий.
