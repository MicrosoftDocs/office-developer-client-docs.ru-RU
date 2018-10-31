---
title: Инструкция UPDATE (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7a761fbc6404cf72818271b956bfc63516942d25
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863285"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="7cbf6-102">Инструкция UPDATE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7cbf6-102">UPDATE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7cbf6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cbf6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7cbf6-104">Создает запрос на обновление, которое изменяет значения в полях в указанной таблице на основании указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cbf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7cbf6-105">Syntax</span></span>

<span data-ttu-id="7cbf6-106">ОБНОВЛЕНИЕ *таблицы* НАБОР *newvalue* WHERE *критериям*;</span><span class="sxs-lookup"><span data-stu-id="7cbf6-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="7cbf6-107">Инструкция UPDATE состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="7cbf6-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cbf6-108">Часть</span><span class="sxs-lookup"><span data-stu-id="7cbf6-108">Part</span></span></p></th>
<th><p><span data-ttu-id="7cbf6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7cbf6-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cbf6-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="7cbf6-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7cbf6-111">Имя таблицы, содержащей данные, которые требуется изменить.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cbf6-112"><em>новое значение</em></span><span class="sxs-lookup"><span data-stu-id="7cbf6-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="7cbf6-113">Выражение, которое определяет значение для вставки в определенное поле обновляемых записей.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cbf6-114"><em>критерии</em></span><span class="sxs-lookup"><span data-stu-id="7cbf6-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="7cbf6-115">Выражение, которое определяет, какие записи будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-115">An expression that determines which records will be updated.</span></span> <span data-ttu-id="7cbf6-116">Обновляются только записи, которые удовлетворяют выражения.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-116">Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7cbf6-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="7cbf6-117">Remarks</span></span>

<span data-ttu-id="7cbf6-118">Обновление особенно полезен при изменяемый большое количество записей или когда записи, которые требуется изменить находятся в нескольких таблиц.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="7cbf6-119">В то же время можно изменить несколько полей.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-119">You can change several fields at the same time.</span></span> <span data-ttu-id="7cbf6-120">В следующем примере увеличивается значения сумма заказа на 10 процентов и значения Доставка на 3 процента для поставщиков в Великобритании:</span><span class="sxs-lookup"><span data-stu-id="7cbf6-120">The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="7cbf6-121">ОБНОВЛЕНИЕ не создает набора результатов.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-121">UPDATE does not generate a result set.</span></span> <span data-ttu-id="7cbf6-122">Кроме того после обновления записей с помощью запроса на обновление нельзя отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-122">Also, after you update records using an update query, you cannot undo the operation.</span></span> <span data-ttu-id="7cbf6-123">Если вы хотите знать, какие записи будут обновлены, выполните результатов выберите запрос, который использует тем же условиям и затем выполните запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-123">If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="7cbf6-124">Создавать резервные копии данных в любое время.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-124">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="7cbf6-125">При обновлении неверный записей, их можно восстановить из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-125">If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="7cbf6-126">Пример</span><span class="sxs-lookup"><span data-stu-id="7cbf6-126">Example</span></span>

<span data-ttu-id="7cbf6-127">В этом примере изменяется значений в поле Подчиняется до 5 для всех записей сотрудников, которые в настоящее время имеют значений подчиняется 2.</span><span class="sxs-lookup"><span data-stu-id="7cbf6-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
