---
title: ADO для классов Windows Foundation (ADO/WFC)
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

ADO для классов Windows Foundation (ADO/WFC) строится на основе модели событий ADO и представляет упрощенный программный интерфейс приложения. Как правило, ADO/WFC перехватывает события ADO, объединяет параметры событий в один класс событий, а затем вызывает обработчик событий.

**Использование событий ADO в ADO/WFC**

1.  Определите собственный обработок событий для обработки события. Например, если вы хотите обработать **событие ConnectComplete** в семейство **ConnectionEvent,** можно использовать этот код:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Определите объект обработки для представления обработера событий. Объект обработки должен иметь тип данных **ConnectEventHandler** для события типа **ConnectionEvent** или тип данных **RecordsetEventHandler** для события типа **RecordsetEvent**. Например, с кодом обработика событий **ConnectComplete** с кодом:
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    Первый аргумент конструктора **ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, именуемого во втором аргументе. Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Первый аргумент конструктора **ConnectionEventHandler** — это ссылка на класс, содержащий обработчик событий, именуемого во втором аргументе. Компилятор Microsoft Visual J++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Единственный аргумент — это ссылка на нужный класс **(этот)** и метод в классе (**onConnectComplete).**

3.  Добавьте обработчик событий в список обработчиков, предназначенных для обработки определенного типа события. Используйте метод с именем, например **addOn***EventName*(*handler).*

4.  ADO/WFC внутренне реализует все обработчики событий ADO. Таким образом, событие, вызванное операцией **Connection** или **Recordset,** перехватывается обработчиком событий ADO/WFC. Обработец событий ADO/WFC передает параметры ADO **ConnectionEvent** в экземпляре класса ADO/WFC **ConnectionEvent** или параметры ADO **RecordsetEvent** в экземпляре класса ADO/WFC **RecordsetEvent.** Эти классы ADO/WFC консолидирует параметры событий ADO; то есть каждый класс ADO/WFC содержит по одному члену данных для каждого уникального параметра во всех методах ADO **ConnectionEvent** или **RecordsetEvent.**

5.  ADO/WFC затем вызывает ваш обработок событий с объектом события ADO/WFC. Например, ваша **подпись обработика onConnectComplete** выглядит так:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    Первый аргумент — это тип объекта, который отправил событие ([Connection](connection-object-ado.md) или [Recordset),](recordset-object-ado.md)а второй аргумент — объект события ADO/WFC (**ConnectionEvent** или **RecordsetEvent).** Подпись обработера событий проще, чем для события ADO. Однако необходимо понимать модель событий ADO, чтобы знать, какие параметры применяются к событию и как реагировать на них.

6.  Возврат из обработки события в обработок ADO/WFC для события ADO. ADO/WFC копирует члены данных о событиях ADO/WFC обратно в параметры события ADO, а затем обработок событий ADO возвращается.

7.  По завершению обработки удалите обработчик из списка обработчиков событий ADO/WFC. Используйте метод с именем, например **removeOn***EventName*(*handler).*

