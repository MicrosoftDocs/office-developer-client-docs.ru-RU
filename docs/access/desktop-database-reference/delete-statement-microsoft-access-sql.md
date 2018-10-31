---
title: Удалите оператор (Microsoft Access SQL)
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
ms.openlocfilehash: 7e41e7597a967e7029cb3ce6ae120bb382714288
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864125"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="58ff1-102">Удалите оператор (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="58ff1-102">DELETE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="58ff1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="58ff1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58ff1-104">Создает запрос на удаление удаляет записи из одной или нескольких таблиц, перечисленных в предложении [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) , которые удовлетворяют предложения [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) .</span><span class="sxs-lookup"><span data-stu-id="58ff1-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause that satisfy the [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ff1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58ff1-105">Syntax</span></span>

<span data-ttu-id="58ff1-106">Удаление \[ *в таблице*. \* \] Из *таблицы* WHERE *критериев*</span><span class="sxs-lookup"><span data-stu-id="58ff1-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="58ff1-107">Оператор DELETE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="58ff1-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="58ff1-108">Часть</span><span class="sxs-lookup"><span data-stu-id="58ff1-108">Part</span></span></p></th>
<th><p><span data-ttu-id="58ff1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="58ff1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58ff1-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="58ff1-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="58ff1-111">Необязательное имя таблицы, из которой удаляются записи.</span><span class="sxs-lookup"><span data-stu-id="58ff1-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58ff1-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="58ff1-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="58ff1-113">Имя таблицы, из которой удаляются записи.</span><span class="sxs-lookup"><span data-stu-id="58ff1-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58ff1-114"><em>критерии</em></span><span class="sxs-lookup"><span data-stu-id="58ff1-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="58ff1-115">Выражение, которое определяет, какие записи для удаления.</span><span class="sxs-lookup"><span data-stu-id="58ff1-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="58ff1-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="58ff1-116">Remarks</span></span>

<span data-ttu-id="58ff1-117">УДАЛИТЬ особенно полезна, если вы хотите удалить несколько записей.</span><span class="sxs-lookup"><span data-stu-id="58ff1-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="58ff1-118">Чтобы удалить всю таблицу из базы данных, можно использовать метод **Execute** с помощью инструкции [DROP](drop-statement-microsoft-access-sql.md) .</span><span class="sxs-lookup"><span data-stu-id="58ff1-118">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="58ff1-119">При удалении таблицы, однако структура будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="58ff1-119">If you delete the table, however, the structure is lost.</span></span> <span data-ttu-id="58ff1-120">С другой стороны при использовании DELETE, удаляется только данные; Структура таблицы и все ее свойства, такие как атрибуты полей и индексы, остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="58ff1-120">In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="58ff1-121">Удалить можно использовать для удаления записи из таблицы, которые находятся в один ко многим отношения с другими таблицами.</span><span class="sxs-lookup"><span data-stu-id="58ff1-121">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables.</span></span> <span data-ttu-id="58ff1-122">Операции каскадного удаления приводят записей в таблицах, которые находятся на разные стороны отношения к удалению при удалении соответствующей записи в одной части отношения в запросе.</span><span class="sxs-lookup"><span data-stu-id="58ff1-122">Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query.</span></span> <span data-ttu-id="58ff1-123">Например в связи между таблицами, клиенты таблицы с одной стороны, находится в таблице заказов на стороне много отношения.</span><span class="sxs-lookup"><span data-stu-id="58ff1-123">For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship.</span></span> <span data-ttu-id="58ff1-124">Удаление записи из результатов клиентов в соответствующие записи заказы, удаляется, если параметр каскадного удаления указанного.</span><span class="sxs-lookup"><span data-stu-id="58ff1-124">Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="58ff1-125">Запрос на удаление удаляет все записи, не данных в определенных полях.</span><span class="sxs-lookup"><span data-stu-id="58ff1-125">A delete query deletes entire records, not just data in specific fields.</span></span> <span data-ttu-id="58ff1-126">Если вы хотите удалить значения конкретного поля, создайте запрос на обновление, которое изменяет значения в **Null**.</span><span class="sxs-lookup"><span data-stu-id="58ff1-126">If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="58ff1-127">После удаления записей с помощью запроса на удаление, нельзя отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="58ff1-127">After you remove records using a delete query, you cannot undo the operation.</span></span> <span data-ttu-id="58ff1-128">Необходимо знать, какие записи будут удалены, выполните результатов выберите запрос, который использует тем же условиям и затем запустите запроса на удаление.</span><span class="sxs-lookup"><span data-stu-id="58ff1-128">If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="58ff1-129">Создавать резервные копии данных в любое время.</span><span class="sxs-lookup"><span data-stu-id="58ff1-129">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="58ff1-130">При удалении неверный записей, их можно восстановить из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="58ff1-130">If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="58ff1-131">Пример</span><span class="sxs-lookup"><span data-stu-id="58ff1-131">Example</span></span>

<span data-ttu-id="58ff1-132">В этом примере удаляются все записи для сотрудников с должностью ученик.</span><span class="sxs-lookup"><span data-stu-id="58ff1-132">This example deletes all records for employees whose title is Trainee.</span></span> <span data-ttu-id="58ff1-133">Если предложение FROM содержит только одну таблицу, нет необходимости списка имя таблицы в инструкции DELETE.</span><span class="sxs-lookup"><span data-stu-id="58ff1-133">When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

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
