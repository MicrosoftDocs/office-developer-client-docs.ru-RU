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
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="320eb-102">Выполнить повторную синхронизацию свойство Command--динамической (ADO)</span><span class="sxs-lookup"><span data-stu-id="320eb-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="320eb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="320eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="320eb-104">Указывает строку пользовательские команды, метод [выполнить повторную синхронизацию](resync-method-ado.md) проблемы для обновления данных в таблице с именем в свойстве динамических [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="320eb-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="320eb-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="320eb-105">Settings and return values</span></span>

<span data-ttu-id="320eb-106">Задает или возвращает **строковое** значение, который является командной строки.</span><span class="sxs-lookup"><span data-stu-id="320eb-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="320eb-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="320eb-107">Remarks</span></span>

<span data-ttu-id="320eb-108">Объект [набора записей](recordset-object-ado.md) производится в результате операции СОЕДИНЕНИЯ на нескольких базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="320eb-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="320eb-109">Измененных строк зависят от параметра *AffectRecords* метода [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="320eb-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="320eb-110">Стандартный метод **выполнить повторную синхронизацию** выполняется, если свойства [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Выполнить повторную синхронизацию команда** не установлены.</span><span class="sxs-lookup"><span data-stu-id="320eb-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="320eb-111">Командную строку свойства **Команда выполнить повторную синхронизацию** параметризованный команду или хранимую процедуру, однозначно идентифицирующее строку обновления и возвращает одну строку, содержащую число и порядок столбцов в виде строки необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="320eb-111">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed.</span></span> <span data-ttu-id="320eb-112">Командная строка содержит параметр для каждого столбца первичного ключа в **Уникальной таблицы**. в противном случае возвращается ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="320eb-112">The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned.</span></span> <span data-ttu-id="320eb-113">Параметры автоматически заполняется значения первичного ключа из строки необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="320eb-113">The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="320eb-114">Ниже приведены два примера на основании SQL:</span><span class="sxs-lookup"><span data-stu-id="320eb-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="320eb-115">**Набор записей** определяется с помощью команды:</span><span class="sxs-lookup"><span data-stu-id="320eb-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="320eb-116">**Команда выполнить повторную синхронизацию** задано значение:</span><span class="sxs-lookup"><span data-stu-id="320eb-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="320eb-117">**Уникальной таблицы** *заказов* , параметризованные первичный ключ, *код заказа*.</span><span class="sxs-lookup"><span data-stu-id="320eb-117">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span> <span data-ttu-id="320eb-118">Подменю выберите предоставляет простой способ программными средствами убедитесь, что же число и порядок столбцов возвращаются как с помощью команды исходного.</span><span class="sxs-lookup"><span data-stu-id="320eb-118">The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="320eb-119">**Набор записей** определяется хранимую процедуру:</span><span class="sxs-lookup"><span data-stu-id="320eb-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="320eb-120">Метод **выполнить повторную синхронизацию** следует выполнить следующую хранимую процедуру:</span><span class="sxs-lookup"><span data-stu-id="320eb-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="320eb-121">**Команда выполнить повторную синхронизацию** задано значение:</span><span class="sxs-lookup"><span data-stu-id="320eb-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="320eb-122">Еще раз **Уникальной таблицы** — *Заказы* и параметризованные первичный ключ, *код заказа*.</span><span class="sxs-lookup"><span data-stu-id="320eb-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="320eb-123">**Команда выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта **набора записей** при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="320eb-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

