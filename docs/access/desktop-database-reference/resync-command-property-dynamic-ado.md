---
title: Динамическое свойство Команды Resync (ADO)
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
# <a name="resync-command-dynamic-property-ado"></a>Динамическое свойство Команды Resync (ADO)

**Область применения**: Access 2013, Office 2013

Указывает командную строку, предоставленную пользователем, которую метод [Resync](resync-method-ado.md) выдает для обновления данных в таблице, указанной в динамическом свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает **строковую** строку, которая является командной строкой.

## <a name="remarks"></a>Примечания

Объект [Recordset](recordset-object-ado.md) является результатом операции JOIN, выполненной на нескольких базовых таблицах. Затронутые строки зависят от *параметра AffectRecords* метода [Resync.](resync-method-ado.md) Стандартный **метод Resync** выполняется, если свойства [команды Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Resync** не установлены.

Строка командной строки свойства **Команды Resync** — это параметризованная команда или сохраненная процедура, которая уникально определяет обновляемую строку и возвращает одну строку, содержащую такое же количество и порядок столбцов, как и строку, которая должна быть обновлена. Строка команд содержит параметр для каждого основного столбца ключа в **уникальной таблице;** в противном случае возвращается ошибка времени запуска. Параметры автоматически заполняются основными ключевыми значениями строки, которые необходимо обновить.

Вот два примера, основанных на SQL:

1.  Набор **записей** определяется командой:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Свойство **Команды Resync** замечено:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    Уникальная **таблица** *— это заказы,* а ее основной ключ *OrderID*— параметризирован. В подказначном выборе предусмотрен простой способ программного обеспечения возврата того же числа и порядка столбцов, что и в исходной команде.

2. Набор **записей** определяется сохраненной процедурой:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    Метод **Resync** должен выполнить следующую сохраненную процедуру:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Свойство **Команды Resync** замечено:

    `"{call CustordersResync (?)}"`

Еще раз повторю, **что уникальная** таблица *— это заказы,* а ее основной ключ *OrderID*— параметризирован.

**Команда Resync —** это динамическое свойство, [](properties-collection-ado.md) применимое к коллекции свойств объектов **Recordset,** когда свойство [CursorLocation](cursorlocation-property-ado.md) задано **для adUseClient.**

