---
title: ADO для Windows классов (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: df9def320274df0eb4636aa237deb566dd5725b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281724"
---
# <a name="adowfc"></a>ADO/WFC


**Область применения**: Access 2013, Office 2013

ADO для Windows классов Foundation (ADO/WFC) строится на модели событий ADO и представляет упрощенный интерфейс программирования приложений. Как правило, ADO/WFC перехватывает события ADO, консолидирует параметры событий в один класс событий и вызывает обработчик событий.

**Использование событий ADO в ADO/WFC**

1.  Определите собственный обработник событий для обработки события. Например, если вы хотите обработать событие **ConnectComplete** в семейство **ConnectionEvent,** можно использовать этот код:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Определите объект обработера, который будет представлять обработник событий. Объект обработки должен быть типа данных **ConnectEventHandler** для события типа **ConnectionEvent** или типа **данных RecordsetEventHandler** для события типа **RecordsetEvent**. Например, закажете следующее для обработика событий **ConnectComplete:**
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    Первый аргумент **конструктора ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, названный во втором аргументе. Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Первый аргумент **конструктора ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, названный во втором аргументе. Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Единственный аргумент — это ссылка на нужный класс **(это)** и метод в классе **(onConnectComplete).**

3.  Добавьте обработчик событий в список обработчиков, назначенных для обработки определенного типа события. Используйте метод с таким именем, как **addOn***EventName**(обработник).*

4.  ADO/WFC внутренне реализует все обработчики событий ADO. Поэтому событие, вызванное операцией **Подключения** или **Recordset,** перехватывает обработчик событий ADO/WFC. Обработник событий ADO/WFC передает параметры ADO **ConnectionEvent** в экземпляре класса ADO/WFC ConnectionEvent или параметры ADO **RecordsetEvent** в экземпляре класса ADO/WFC **RecordsetEvent.**  Эти классы ADO/WFC консолидировать параметры событий ADO; то есть каждый класс ADO/WFC содержит по одному члену данных для каждого уникального параметра во всех методах ADO **ConnectionEvent** или **RecordsetEvent.**

5.  Затем ADO/WFC вызывает обработник событий с объектом события ADO/WFC. Например, обработник **onConnectComplete** имеет подпись:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    Первый аргумент — тип объекта, отправив событие [(Подключение](connection-object-ado.md) или Набор записей), [](recordset-object-ado.md)а второй аргумент — объект события ADO/WFC **(ConnectionEvent** или **RecordsetEvent).** Подпись обработера событий проще, чем событие ADO. Однако для того, чтобы узнать, какие параметры применяются к событию и как реагировать, необходимо понять модель событий ADO.

6.  Вернись из обработки событий в обработник ADO/WFC для события ADO. ADO/WFC копирует устроимые участники событий ADO/WFC обратно в параметры событий ADO, а затем обработник событий ADO возвращается.

7.  После завершения обработки удалите обработчик из списка обработчиков событий ADO/WFC. Используйте метод с таким именем, как **removeOn***EventName**(обработник).*

