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
# <a name="resync-command-dynamic-property-ado"></a><span data-ttu-id="115bb-102">Динамическое свойство Resync Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="115bb-102">Resync Command dynamic property (ADO)</span></span>

<span data-ttu-id="115bb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="115bb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="115bb-104">Указывает предоставленную пользователем строку команды, которую метод [Resync](resync-method-ado.md) выдает для обновления данных в таблице с именем в динамическом свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="115bb-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="115bb-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="115bb-105">Settings and return values</span></span>

<span data-ttu-id="115bb-106">Задает или возвращает **строку,** которая является строкой команды.</span><span class="sxs-lookup"><span data-stu-id="115bb-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="115bb-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="115bb-107">Remarks</span></span>

<span data-ttu-id="115bb-108">Объект [Recordset](recordset-object-ado.md) является результатом операции JOIN, выполненной в нескольких базовых таблицах.</span><span class="sxs-lookup"><span data-stu-id="115bb-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="115bb-109">Затронутые строки зависят *от параметра AffectRecords* метода [Resync.](resync-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="115bb-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="115bb-110">Стандартный **метод Resync** выполняется, если свойства [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) и **Resync Command** не за установлены.</span><span class="sxs-lookup"><span data-stu-id="115bb-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="115bb-111">Строка команды свойства **Resync Command** — это параметризованная команда или хранимая процедура, которая уникальным образом определяет обновляемую строку и возвращает одну строку, содержащую такое же количество и порядок столбцов, что и обновляемая строка.</span><span class="sxs-lookup"><span data-stu-id="115bb-111">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed.</span></span> <span data-ttu-id="115bb-112">Строка команды содержит параметр для каждого столбца первичного ключа в **уникальной таблице;** в противном случае возвращается ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="115bb-112">The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned.</span></span> <span data-ttu-id="115bb-113">Параметры автоматически заполняются значениями первичного ключа из обновляемой строки.</span><span class="sxs-lookup"><span data-stu-id="115bb-113">The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="115bb-114">Вот два примера, основанных на SQL:</span><span class="sxs-lookup"><span data-stu-id="115bb-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="115bb-115">Набор **записей** определяется командой:</span><span class="sxs-lookup"><span data-stu-id="115bb-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="115bb-116">Свойство **Resync Command** имеет:</span><span class="sxs-lookup"><span data-stu-id="115bb-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="115bb-117">Уникальная **таблица** *— заказы,* а ее первичный ключ *OrderID* задан.</span><span class="sxs-lookup"><span data-stu-id="115bb-117">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span> <span data-ttu-id="115bb-118">В поднабираемом пункте предусмотрен простой способ программным способом обеспечить возвращение того же числа и порядка столбцов, что и в исходной команде.</span><span class="sxs-lookup"><span data-stu-id="115bb-118">The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="115bb-119">Набор **записей** определяется хранимой процедурой:</span><span class="sxs-lookup"><span data-stu-id="115bb-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="115bb-120">Метод **Resync** должен выполнить следующую хранимую процедуру:</span><span class="sxs-lookup"><span data-stu-id="115bb-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="115bb-121">Свойство **Resync Command** имеет:</span><span class="sxs-lookup"><span data-stu-id="115bb-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="115bb-122">Опять же, **уникальная таблица** *— заказы,* а ее первичный ключ *OrderID*— задан.</span><span class="sxs-lookup"><span data-stu-id="115bb-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="115bb-123">**Resync Command** — это динамическое свойство, [](properties-collection-ado.md) которое применится к коллекции свойств объекта **Recordset,** когда свойству [CursorLocation](cursorlocation-property-ado.md) задано свойство **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="115bb-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

