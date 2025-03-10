# hse_hw2_chip


# Основная часть
[Ссылка на основную часть гугл коллаб](https://colab.research.google.com/drive/1pGWjxTGfYP6aowHGAn_3wu2aT8qb-J86?authuser=2#scrollTo=0mOfy-cbtyog)
[Ccылка на сравнение результатов и бонусную часть](https://colab.research.google.com/drive/1tDhpZplVbDVBcQaChzt9HFF9GaoIKPnx?usp=sharing)

## Описание клеточной линии

#### Тип ткани:
- Клеточная линия WA01 (H1-hESC) — одна из первых и наиболее широко используемых линий эмбриональных стволовых клеток человека. Эти клетки являются плюрипотентными, то есть способны дифференцироваться в любые типы клеток организма (эндодерма, мезодерма, эктодерма).

#### Пол:
- Мужской
  
#### Возраст на момент забора:
- Стадия бластоцисты (около 5–6 дней после оплодотворения)

## Fastqc


В данном случае обрезание чтение было необходимо так как их изначальное качество не самое хорошее
#### Результаты до триммирования
<div style="display: flex; justify-content: space-between;">
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 15" src="https://github.com/user-attachments/assets/42035d55-002d-4dbb-8bf2-9b93841c8c1d" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 25" src="https://github.com/user-attachments/assets/fe3876ec-7123-474d-8f46-d4bfd5639a06" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 37" src="https://github.com/user-attachments/assets/67693e6a-b21e-481f-86b3-1c62e1a2003a" />
</div>

После работы trimmomatic практически по всем параметрам триммированные данные прошли проверку на качества, из чего делаем вывод, что обрезание чтений прошло успешно!
#### Результаты после триммирования 
<div style="display: flex; justify-content: space-between;">
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 25 03" src="https://github.com/user-attachments/assets/ec8aadc8-b43d-4be6-a129-8875108c585a" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 25 19" src="https://github.com/user-attachments/assets/c2f241dd-3c3f-4ed5-a2ac-01bd6b07dee3" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 25 25" src="https://github.com/user-attachments/assets/d71081f9-d8f6-474d-9363-1e82ab076aae" />
</div>

## Таблица со статистикой по каждому из  образцов:

| Заголовок 1 | 1 реплика (ENCFF137PVL) | 2 реплика (ENCFF171DUV) | контроль (ENCFF176RJQ) |
|:-----------:|:-----------:|:-----------:|:-----------:|
| Всего ридов    | 8874861 (100%)    | 19825041 (100%)   | 9357767 (100.00%)    |
| Уникально выравненные    | 396647 (4.47%)    | 588740 (2.97%)    | 242561 (2.59%)    |
| Не уникально выравненные   | 1216103 (13.70%)  | 2309185 (11.65%)   | 831645 (8.89%)   |
| Не выравнилось   | 7262111 (81.83%)   | 16927116 (85.38%)   | 8283561 (88.52%)   |

Процент выравнивания получился таким низким вследствие того, что оно проводилось только на одну хромосому (14 в данном случае), а не на весь геном из-за ограниченных ресурсов.

## Диаграммы Венна 

Не переименовывала файлы в коде, поэтому вот уточнение по результатам:
ASU = ENCFF137PVL
ARK = ENCFF171DUV 

<img width="813" alt="Снимок экрана 2025-03-09 в 23 32 09" src="https://github.com/user-attachments/assets/613136f0-190d-4fd6-9329-6dfb982d24db" />
<img width="956" alt="Снимок экрана 2025-03-09 в 23 32 20" src="https://github.com/user-attachments/assets/8918fcaf-2dd9-4a16-85b6-24075c86f2fd" />


В данных репликах было не такое большое количество пиков из-за выравнивания только на одну хромосому 14 из-за ограниченных ресурсов, однако образец ENCODE был выровнен на все хромосомы, соответственно, имеет гораздо большее количество пиков.


# Бонус 1

<img width="563" alt="Снимок экрана 2025-03-09 в 21 45 13" src="https://github.com/user-attachments/assets/fbfb5f80-c991-4b91-9d3e-f5ff7051d77c" />

### Результаты по скачанным .BigWig .Bam

![result-2](https://github.com/user-attachments/assets/dbe99654-0e04-4ce9-9094-82acdd738095)
![result-3](https://github.com/user-attachments/assets/1d16eba1-24c5-4367-b9ef-7fc5a862fbff)

### Результат по .BigWig полученного из .Bam в коллабе

![result](https://github.com/user-attachments/assets/25330720-8f76-4e2b-8e33-a4986edefead)

### Вывод

Все три полученных графика в целом совпадают с теоретической информацией, так как мы видим пик вначале, который впоследствие затухает.


# Бонус 2

#### Воспроизводимость пиков
![output txt](https://github.com/user-attachments/assets/b7fab6d2-3ba0-4fc3-834a-dae766451ee8)

Верхний левый график - соотношение рангов пиков в образцах. Большинство точек бледные, поэтому хорошая воспроизводимость (если IDR > 0.05 , то точки окрашены в красный - менее воспроизводимые пики)
Нижние графики показывают распределение IDR по рангам пиков в обоих образцах. 

Большинство пиков имеют низкие значения IDR => есть хорошая воспроизводимость

![Unknown](https://github.com/user-attachments/assets/4b514ba5-7a04-4860-b024-41fdd4aa93e5)


