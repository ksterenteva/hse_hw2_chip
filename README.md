# hse_hw2_chip

# Основная часть 

## Описание клеточной линии

#### Тип ткани
- Клеточная линия WA01 (H1-hESC) — одна из первых и наиболее широко используемых линий эмбриональных стволовых клеток человека. Эти клетки являются плюрипотентными, то есть способны дифференцироваться в любые типы клеток организма (эндодерма, мезодерма, эктодерма).

#### Пол:
- Мужской
  
#### Возраст на момент забора:
- Стадия бластоцисты (около 5–6 дней после оплодотворения)

## Fastqc

#### Результаты до триммирования
<div style="display: flex; justify-content: space-between;">
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 15" src="https://github.com/user-attachments/assets/42035d55-002d-4dbb-8bf2-9b93841c8c1d" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 25" src="https://github.com/user-attachments/assets/fe3876ec-7123-474d-8f46-d4bfd5639a06" />
<img width="30%" alt="Снимок экрана 2025-03-09 в 21 23 37" src="https://github.com/user-attachments/assets/67693e6a-b21e-481f-86b3-1c62e1a2003a" />
</div>

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

## Диаграммы Венна 

Не переименовывала файлы в коде, поэтому вот уточнение по результатам:
ASU = ENCFF137PVL
ARK = ENCFF171DUV 

[Intervene_venn-3.pdf](https://github.com/user-attachments/files/19151392/Intervene_venn-3.pdf)

[Intervene_venn-4.pdf](https://github.com/user-attachments/files/19151393/Intervene_venn-4.pdf)

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



