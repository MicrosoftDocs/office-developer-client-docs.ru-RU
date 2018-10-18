---
title: Resync Command Property--Dynamic (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d9133f37b236cfa876a5d6ae8642f25f919f2cb
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602806"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="a31ad-102">Resync Command Property--Dynamic (ADO)</span><span class="sxs-lookup"><span data-stu-id="a31ad-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="a31ad-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a31ad-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a31ad-104">Указывает строку пользовательские команды, метод [выполнить повторную синхронизацию](resync-method-ado.md) проблемы для обновления данных в таблице с именем в свойстве динамических [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a31ad-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

<span data-ttu-id="a31ad-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a31ad-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="a31ad-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a31ad-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="a31ad-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a31ad-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="a31ad-108">master</span><span class="sxs-lookup"><span data-stu-id="a31ad-108">master</span></span>

<span data-ttu-id="a31ad-109">Задает или возвращает **строковое** значение, который является командной строки.</span><span class="sxs-lookup"><span data-stu-id="a31ad-109">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="a31ad-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="a31ad-110">Remarks</span></span>

<span data-ttu-id="a31ad-111">Объект [набора записей](recordset-object-ado.md) производится в результате операции СОЕДИНЕНИЯ на нескольких базовых таблиц.</span><span class="sxs-lookup"><span data-stu-id="a31ad-111">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="a31ad-112">Измененных строк зависят от параметра *AffectRecords* метода [выполнить повторную синхронизацию](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a31ad-112">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="a31ad-113">Стандартный метод **выполнить повторную синхронизацию** выполняется, если свойства [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Выполнить повторную синхронизацию команда** не установлены.</span><span class="sxs-lookup"><span data-stu-id="a31ad-113">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="a31ad-114">Командную строку свойства **Команда выполнить повторную синхронизацию** параметризованный команду или хранимую процедуру, однозначно идентифицирующее строку обновления и возвращает одну строку, содержащую число и порядок столбцов в виде строки необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="a31ad-114">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed.</span></span> <span data-ttu-id="a31ad-115">Командная строка содержит параметр для каждого столбца первичного ключа в **Уникальной таблицы**. в противном случае возвращается ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a31ad-115">The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned.</span></span> <span data-ttu-id="a31ad-116">Параметры автоматически заполняется значения первичного ключа из строки необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="a31ad-116">The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="a31ad-117">Ниже приведены два примера на основании SQL:</span><span class="sxs-lookup"><span data-stu-id="a31ad-117">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="a31ad-118">**Набор записей** определяется с помощью команды:</span><span class="sxs-lookup"><span data-stu-id="a31ad-118">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="a31ad-119">**Команда выполнить повторную синхронизацию** задано значение:</span><span class="sxs-lookup"><span data-stu-id="a31ad-119">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="a31ad-120">**Уникальной таблицы** *заказов* , параметризованные первичный ключ, *код заказа*.</span><span class="sxs-lookup"><span data-stu-id="a31ad-120">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span> <span data-ttu-id="a31ad-121">Подменю выберите предоставляет простой способ программными средствами убедитесь, что же число и порядок столбцов возвращаются как с помощью команды исходного.</span><span class="sxs-lookup"><span data-stu-id="a31ad-121">The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="a31ad-122">**Набор записей** определяется хранимую процедуру:</span><span class="sxs-lookup"><span data-stu-id="a31ad-122">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="a31ad-123">Метод **выполнить повторную синхронизацию** следует выполнить следующую хранимую процедуру:</span><span class="sxs-lookup"><span data-stu-id="a31ad-123">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="a31ad-124">**Команда выполнить повторную синхронизацию** задано значение:</span><span class="sxs-lookup"><span data-stu-id="a31ad-124">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="a31ad-125">Еще раз **Уникальной таблицы** — *Заказы* и параметризованные первичный ключ, *код заказа*.</span><span class="sxs-lookup"><span data-stu-id="a31ad-125">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="a31ad-126">**Команда выполнить повторную синхронизацию** является динамическим добавляется в конец коллекции [свойств](properties-collection-ado.md) объекта **набора записей** при [CursorLocation](cursorlocation-property-ado.md) задано значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="a31ad-126">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

