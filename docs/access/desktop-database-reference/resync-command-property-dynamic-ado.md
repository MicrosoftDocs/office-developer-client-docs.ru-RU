---
title: Выполнить повторную синхронизацию свойство Command--динамической (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 30707140284c4c4fda157e276e62666f0344ad14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872006"
---
# <a name="resync-command-property--dynamic-ado"></a>Выполнить повторную синхронизацию свойство Command--динамической (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает строку пользовательские команды, метод [выполнить повторную синхронизацию](resync-method-ado.md) проблемы для обновления данных в таблице с именем в свойстве динамических [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, который является командной строки.

## <a name="remarks"></a>Замечания

Объект [набора записей](recordset-object-ado.md) производится в результате операции СОЕДИНЕНИЯ на нескольких базовых таблиц. Измененных строк зависят от параметра *AffectRecords* метода [выполнить повторную синхронизацию](resync-method-ado.md) . Стандартный метод **выполнить повторную синхронизацию** выполняется, если свойства [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Выполнить повторную синхронизацию команда** не установлены.

Командную строку свойства **Команда выполнить повторную синхронизацию** параметризованный команду или хранимую процедуру, однозначно идентифицирующее строку обновления и возвращает одну строку, содержащую число и порядок столбцов в виде строки необходимо обновить. Командная строка содержит параметр для каждого столбца первичного ключа в **Уникальной таблицы**. в противном случае возвращается ошибка во время выполнения. Параметры автоматически заполняется значения первичного ключа из строки необходимо обновить.

Ниже приведены два примера на основании SQL:

1.  **Набор записей** определяется с помощью команды:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    **Команда выполнить повторную синхронизацию** задано значение:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    **Уникальной таблицы** *заказов* , параметризованные первичный ключ, *код заказа*. Подменю выберите предоставляет простой способ программными средствами убедитесь, что же число и порядок столбцов возвращаются как с помощью команды исходного.

2. **Набор записей** определяется хранимую процедуру:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    Метод **выполнить повторную синхронизацию** следует выполнить следующую хранимую процедуру:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    **Команда выполнить повторную синхронизацию** задано значение:

    `"{call CustordersResync (?)}"`

Еще раз **Уникальной таблицы** — *Заказы* и параметризованные первичный ключ, *код заказа*.

**Команда выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта **набора записей** при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.

