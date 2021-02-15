---
title: Динамическое свойство Resync Command (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306582"
---
# <a name="resync-command-dynamic-property-ado"></a>Динамическое свойство Resync Command (ADO)

**Область применения**: Access 2013, Office 2013

Указывает предоставленную пользователем строку команды, которую метод [Resync](resync-method-ado.md) выдает для обновления данных в таблице с именем в динамическом свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строку,** которая является строкой команды.

## <a name="remarks"></a>Заметки

Объект [Recordset](recordset-object-ado.md) является результатом операции JOIN, выполненной в нескольких базовых таблицах. Затронутые строки зависят *от параметра AffectRecords* метода [Resync.](resync-method-ado.md) Стандартный **метод Resync** выполняется, если свойства [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Resync Command** не за установлены.

Строка команды свойства **Resync Command** — это параметризованная команда или хранимая процедура, которая уникальным образом определяет обновляемую строку и возвращает одну строку, содержащую такое же количество и порядок столбцов, что и обновляемая строка. Строка команды содержит параметр для каждого столбца первичного ключа в **уникальной таблице;** в противном случае возвращается ошибка времени запуска. Параметры автоматически заполняются значениями первичного ключа из обновляемой строки.

Вот два примера, основанных на SQL:

1.  Набор **записей** определяется командой:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Свойство **Resync Command** имеет:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    Уникальная **таблица** *— заказы,* а ее первичный ключ *OrderID* задан. В поднабираемом пункте предусмотрен простой способ программным способом обеспечить возвращение того же числа и порядка столбцов, что и в исходной команде.

2. Набор **записей** определяется хранимой процедурой:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    Метод **Resync** должен выполнить следующую хранимую процедуру:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Свойство **Resync Command** имеет:

    `"{call CustordersResync (?)}"`

Опять же, **уникальная таблица** *— заказы,* а ее первичный ключ *OrderID*— задан.

**Resync Command** — это динамическое свойство, [](properties-collection-ado.md) которое применится к коллекции свойств объекта **Recordset,** когда свойству [CursorLocation](cursorlocation-property-ado.md) задано свойство **adUseClient.**

