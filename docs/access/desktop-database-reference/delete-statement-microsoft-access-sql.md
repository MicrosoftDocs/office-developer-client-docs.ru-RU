---
title: Оператор DELETE (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a4ef478e74f9851012d6f749e64b4ddb34f3a959
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715623"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="08931-102">Оператор DELETE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="08931-102">DELETE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="08931-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08931-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08931-104">Создает запрос на удаление, который удаляет записи из одной или нескольких таблиц, указанных в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql), отвечающих предложению [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span><span class="sxs-lookup"><span data-stu-id="08931-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause that satisfy the [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="08931-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08931-105">Syntax</span></span>

<span data-ttu-id="08931-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span><span class="sxs-lookup"><span data-stu-id="08931-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="08931-107">Оператор DELETE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="08931-107">The For…Next statement syntax has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08931-108">Часть</span><span class="sxs-lookup"><span data-stu-id="08931-108">Part</span></span></p></th>
<th><p><span data-ttu-id="08931-109">Описание</span><span class="sxs-lookup"><span data-stu-id="08931-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08931-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="08931-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="08931-111">Необязательное имя таблицы, из которой удаляются записи.</span><span class="sxs-lookup"><span data-stu-id="08931-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08931-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="08931-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="08931-113">Имя таблицы, из которой удаляются записи.</span><span class="sxs-lookup"><span data-stu-id="08931-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08931-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="08931-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="08931-115">Выражение, определяющее, какие записи нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="08931-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="08931-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08931-116">Remarks</span></span>

<span data-ttu-id="08931-117">DELETE особенно полезен, если вы хотите удалить большое количество записей.</span><span class="sxs-lookup"><span data-stu-id="08931-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="08931-118">Чтобы удалить всю таблицу из базы данных, можно использовать метод **Execute** с оператором [DROP](drop-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="08931-118">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="08931-119">Однако, если удалить таблицу, может потеряться структура.</span><span class="sxs-lookup"><span data-stu-id="08931-119">If you delete the table, however, the structure is lost.</span></span> <span data-ttu-id="08931-120">С другой стороны при использовании DELETE удаляются только данные; а структура таблицы и все ее свойства, такие как атрибуты поля и индексы, остаются нетронутыми.</span><span class="sxs-lookup"><span data-stu-id="08931-120">In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="08931-121">Вы можете использовать DELETE, чтобы удалить записи из таблиц, которые находятся в связи "один ко многим" с другими таблицами.</span><span class="sxs-lookup"><span data-stu-id="08931-121">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables.</span></span> <span data-ttu-id="08931-122">Операции каскадного удаления вызывают удаление записей в таблицах, расположенных на стороне многих связей, при удалении соответствующей записи на стороне одной связи при запросе.</span><span class="sxs-lookup"><span data-stu-id="08931-122">Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query.</span></span> <span data-ttu-id="08931-123">Например, в связи между таблицами Клиенты и Заказы, таблица Клиенты находится на стороне одной связи, а таблица Заказы находится на стороне многих связей.</span><span class="sxs-lookup"><span data-stu-id="08931-123">For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship.</span></span> <span data-ttu-id="08931-124">Удаление записи из результатов клиентов в соответствующих записях заказов, удаляемых в случае, если указан параметр каскадного удаления.</span><span class="sxs-lookup"><span data-stu-id="08931-124">Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="08931-125">Запрос на удаление удаляет записи целиком, а не только данные в определенных полях.</span><span class="sxs-lookup"><span data-stu-id="08931-125">A delete query deletes entire records, not just data in specific fields.</span></span> <span data-ttu-id="08931-126">Если вы хотите удалить значения в определенном поле, создайте обновленный запрос, который изменяет значение на **Null**.</span><span class="sxs-lookup"><span data-stu-id="08931-126">If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="08931-127">После удаления записи с помощью запроса на удаление невозможно отменить данную операцию.</span><span class="sxs-lookup"><span data-stu-id="08931-127">After you remove records using a delete query, you cannot undo the operation.</span></span> <span data-ttu-id="08931-128">Если вы хотите узнать, какие записи были удалены, сначала проверьте результаты запроса на выборку, в котором используется то же самое условие, и снова запустите запрос на удаление.</span><span class="sxs-lookup"><span data-stu-id="08931-128">If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="08931-129">Сохраняйте резервные копии ваших данных в любое время.</span><span class="sxs-lookup"><span data-stu-id="08931-129">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="08931-130">Если вы удалили не те записи, вы сможете восстановить их из резервных копий.</span><span class="sxs-lookup"><span data-stu-id="08931-130">If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="08931-131">Пример</span><span class="sxs-lookup"><span data-stu-id="08931-131">Example</span></span>

<span data-ttu-id="08931-132">В этом примере будут удалены все записи для сотрудников, чья должность — стажер.</span><span class="sxs-lookup"><span data-stu-id="08931-132">This example deletes all records for employees whose title is Trainee.</span></span> <span data-ttu-id="08931-133">Если оператор FROM содержит только одну таблицу, нет необходимости перечислять имя таблицы в операторе DELETE.</span><span class="sxs-lookup"><span data-stu-id="08931-133">When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```
