---
title: Динамическое свойство команды Resync (ADO)
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
# <a name="resync-command-dynamic-property-ado"></a>Динамическое свойство команды Resync (ADO)

**Область применения**: Access 2013, Office 2013

Задает пользовательскую строку команды, которая выдает метод [Resync](resync-method-ado.md) для обновления данных в таблице, имя которой указано в динамическом свойстве [таблицы Unique](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, представляющее собой командную строку.

## <a name="remarks"></a>Примечания

Объект [Recordset](recordset-object-ado.md) является результатом операции JOIN, выполняемой над несколькими базовыми таблицами. Затронутые строки зависят от параметра *аффектрекордс* метода [Resync](resync-method-ado.md) . Стандартный метод **Resync** выполняется, если не заданы свойства " [уникальная таблица](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) " и " **Повторная синхронизация** ".

Командная строка свойства Command повторной **синхронизации** — это параметризованная команда или хранимая процедура, однозначно определяющая обновляемую строку, а также возвращающая одну строку, содержащую то же число и порядок столбцов, что и обновляемая строка. Командная строка содержит параметр для каждого столбца первичного ключа в **уникальной таблице**; в противном случае возвращается ошибка времени выполнения. Параметры автоматически заполняются значениями первичного ключа из обновляемой строки.

Ниже приведено два примера, основанных на SQL:

1.  **Набор записей** определяется с помощью команды.

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Для свойства **команды Resync** задано значение:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    **Уникальная таблица** *Orders* и ее первичный ключ, *OrderID*, параметризованы. Вложенный выбор предоставляет простой способ программного обеспечения, чтобы программным способом убедиться в том, что одно и то же число и порядок столбцов возвращаются как исходная команда.

2. **Набор записей** определяется хранимой процедурой.

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    Метод **Resync** должен выполнять следующую хранимую процедуру:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Для свойства **команды Resync** задано значение:

    `"{call CustordersResync (?)}"`

Опять же, **уникальная таблица** — *Orders* , а ее первичный ключ, *OrderID*— параметризованным.

**Команда Resync** — это динамическое свойство, добавленное в коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** , если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.

