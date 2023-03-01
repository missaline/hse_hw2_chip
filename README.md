# hse_hw2_chip

[Cсылка на Google Colab](https://colab.research.google.com/drive/15rEjxXaykKNq35XRub3ahqK362aUOacm?usp=sharing)

Для домашнего задания был выбран эксперимент на пересечении клеточной линии HepG2 и гистоновой метки H3K4me3. 
Были использованы следующие данные: 
- 1 реплика: ENCFF001FMH
- 2 реплика: ENCFF001FMG
- контроль: ENCFF001HOD

## FastQC
| ENCFF001FMG |   ENCFF001FMH   | ENCFF001HOD | 
| -------------- | :-----: | :-------------------------: | 
| ![image](https://user-images.githubusercontent.com/104971016/222193110-e0604722-7615-4edb-b0f8-37e88b1537b1.png)| ![image](https://user-images.githubusercontent.com/104971016/222194539-a8724eed-b3a0-46eb-921c-add9cbbd11bc.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195226-e3a22ff9-f58b-4526-8c03-ab51c7089a03.png)  |
| ![image](https://user-images.githubusercontent.com/104971016/222193907-39e7a441-239f-4066-8514-5ea95b64a433.png) | ![image](https://user-images.githubusercontent.com/104971016/222194823-ab5939fd-a0ef-4f94-b27f-5fe52576c471.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195326-ad2e32e2-02ea-40f8-9a25-04e034cb4f72.png)  |
| ![image](https://user-images.githubusercontent.com/104971016/222193998-ad96159d-713f-4ded-9c0b-b1f03e289304.png) | ![image](https://user-images.githubusercontent.com/104971016/222194890-194aba03-9918-4c26-9724-340150699803.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195453-ad2233c4-164f-4662-8329-8f472a6c3427.png)  |
| ![image](https://user-images.githubusercontent.com/104971016/222194075-852ef71b-366c-4fe5-b0bd-4d64b58acdba.png) | ![image](https://user-images.githubusercontent.com/104971016/222194959-1c1b0781-3481-4cbe-95a4-e7659eade50b.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195526-d3728422-c55b-4c31-afa3-3edb4aadbf19.png)  |
| ![image](https://user-images.githubusercontent.com/104971016/222194205-dc1500b2-f2ea-446a-ba6c-400e04e24125.png) | ![image](https://user-images.githubusercontent.com/104971016/222195031-c05366b5-380d-42ef-b9d2-d5ad771c449f.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195617-7753396f-975d-481b-adb3-31242f950d9d.png)  |
| ![image](https://user-images.githubusercontent.com/104971016/222194293-8e9964c5-5b37-4d5c-b292-8b373c7a5871.png) | ![image](https://user-images.githubusercontent.com/104971016/222195124-5ba784fb-ab98-4cf1-9420-3ba80bb7801f.png) |  ![image](https://user-images.githubusercontent.com/104971016/222195690-59a06b24-c831-42bb-addf-bab39da18434.png)  |

Качество ридов хорошее, поэтому этап подрезания был пропущен.


## Таблица с информацией по образцам  
| ID             |   Общее число ридов   | Выровнившиеся уникально | Выровнившиеся уникально (%) | Выровнившиеся неуникально | Выровнившиеся неуникально (%) | Не выровнившиеся | Не выровнившиеся (%) |
| -------------- | :-----: | :-------------------------: | :------------------------------------------------------------: | :---------------------------------------------------------: | :----------------------------------: | :----------------------------------: | :----------------------------------: |
| **ENCFF001FMH** | 16375803 |  953573  |  5.82  |  950204  |  5.80  |  14472026  |  88.37  |
| **ENCFF001FMG** | 16380903 |  965888  |  5.90  |  989033  |  6.04  |  14425982  |  88.07  |
| **ENCFF001HOD** | 18282579 |  809680  |  4.43  |  2491233  |  13.63  |  14981666 |  81.95  |

Доля выравниваний получилась достаточно низкой из-за выравнивания только по одной хромосоме, а не по всему геному.

## Диаграммы Эйлера-Венна
| 1 реплика с ENCODE | ENCODE с 1 репликой | 2 реплика с ENCODE | ENCODE с 2 репликой |
| -------------- | :-----: | :-----: | :-----: |
| ![image](https://user-images.githubusercontent.com/104971016/222198399-82db99a6-8576-4485-b042-b1b32f1453fd.png) | ![image](https://user-images.githubusercontent.com/104971016/222200032-4dfd3ce8-9d6a-4948-a5f1-ba3429defa60.png) | ![image](https://user-images.githubusercontent.com/104971016/222201346-774af953-b88b-4b16-a00e-8e2f2a3e86d6.png) | ![image](https://user-images.githubusercontent.com/104971016/222201443-9a33bf0b-5af7-4434-959e-a0b685f707d0.png) |

Пересечений довольно мало, это может быть связано с тем, что выравнивание производилось только на одну хромосому. В базе данных ENCODE пики составлены для всех хромосом, поэтому их намного больше, из-за чего и наблюдаются различия с нашими результатами

## Бонус

| ENCFF479BJO | ENCFF342FTF |
| -------------- | :-----: |
| ![ngs_plot1](https://user-images.githubusercontent.com/104971016/222205410-1c773eb7-f0b4-4865-ba2a-f09f8539c9fe.png) | ![ngs_plot2](https://user-images.githubusercontent.com/104971016/222205879-c3599fad-90b6-4360-9c53-6e6dd959cc39.png) |
