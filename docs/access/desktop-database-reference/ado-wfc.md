---
title: ADO для классов Windows Foundation (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd5b54160bfa6c692bfcd6489646021dcce34631
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481575"
---
# <a name="adowfc"></a>ADO/WFC


**Применимо к**: Access 2013 | Office 2013

ADO для Windows классов (ADO/WFC) основана на модели событий ADO и представляет упрощенный интерфейс программирования. В общем случае ADO/WFC перехватывает события ADO, объединяет параметры события в классе событий и затем вызывает обработчик события.

**Чтобы использовать события ADO в ADO/WFC**

1.  Определите обработчик событий для обработки события. Например если вы хотите обрабатывать события **ConnectComplete** семейства **ConnectionEvent** , могут используйте следующий код:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Определите объект обработчика для представления обработчик событий. Объект обработчика должен иметь тип данных **ConnectEventHandler** для события типа **ConnectionEvent**или тип данных **RecordsetEventHandler** для события типа **RecordsetEvent**. Например код следующие параметры для обработчика событий **ConnectComplete** :
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    Первый аргумент конструктора **ConnectionEventHandler** является ссылкой на класс, который содержит обработчик событий с именем в качестве второго аргумента. Компилятор Microsoft Visual J ++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Первый аргумент конструктора **ConnectionEventHandler** является ссылкой на класс, который содержит обработчик событий с именем в качестве второго аргумента. Компилятор Microsoft Visual J ++ также поддерживает эквивалентный синтаксис:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    Один аргумент является ссылкой на нужный класс (**в этом**) и метода в класс (**onConnectComplete**).

3.  Добавление обработчика событий в список обработчиков, предназначенный для обработки конкретного типа событий. Например, используйте метод с именем **дополнительный компонент *** EventName*(*обработчик*).

4.  ADO/WFC во внутренней сети реализует все обработчики событий ADO. Таким образом с помощью обработчика событий ADO/WFC перехватывает события, вызванные операции **подключения** или **набора записей** . Обработчик событий ADO/WFC передает параметры ADO **ConnectionEvent** в экземпляр класса ADO/WFC **ConnectionEvent** или параметры ADO **RecordsetEvent** в экземпляр класса ADO/WFC **RecordsetEvent** . Эти классы ADO/WFC консолидировать параметры события ADO; то есть каждый класс ADO/WFC содержит один элемент данных для каждого уникального параметра в ADO **ConnectionEvent** или **RecordsetEvent** методов.

5.  ADO/WFC вызывает обработчик событий с помощью объекта ADO/WFC события. Например обработчик **onConnectComplete** имеет подпись следующим образом:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    Первый аргумент — это тип объекта, отправляющий событие ([подключения](connection-object-ado.md) или [набора записей](recordset-object-ado.md)), а второй аргумент — это объект ADO/WFC событий (**ConnectionEvent** или **RecordsetEvent**). Подпись обработчика событий проще, чем событие ADO. Тем не менее по-прежнему необходимо понять модели событий ADO узнать параметры применяются к событию и о реагировании.

6.  Возвращает из обработчика событий ADO/WFC обработчик для события ADO. ADO/WFC копирует соответствующие элементы данных ADO/WFC событие обратно в параметры события ADO и возвращает обработчик события ADO.

7.  Завершении обработки, удалите обработчик из списка ADO/WFC обработчиков событий. Например, используйте метод с именем **removeOn *** EventName*(*обработчик*).

