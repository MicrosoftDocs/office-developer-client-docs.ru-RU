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
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717232"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="c4583-102">Инструкция UPDATE (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c4583-102">UPDATE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c4583-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4583-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4583-104">Создает запрос на обновление, который изменяет значения в полях в указанной таблице на основании заданных условий.</span><span class="sxs-lookup"><span data-stu-id="c4583-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4583-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4583-105">Syntax</span></span>

<span data-ttu-id="c4583-106">UPDATE *таблица* SET *новое_значение* WHERE *критерии*;</span><span class="sxs-lookup"><span data-stu-id="c4583-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="c4583-107">Инструкция UPDATE состоит из трех указанных ниже частей.</span><span class="sxs-lookup"><span data-stu-id="c4583-107">The For…Next statement syntax has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4583-108">Часть</span><span class="sxs-lookup"><span data-stu-id="c4583-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c4583-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c4583-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4583-110"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="c4583-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c4583-111">Имя таблицы, содержащей данные, которые необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="c4583-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4583-112"><em>новое_значение</em></span><span class="sxs-lookup"><span data-stu-id="c4583-112"><em>newValue</em></span></span></p></td>
<td><p><span data-ttu-id="c4583-113">Выражение, указывающее значение, которое необходимо вставить в определенное поле обновляемых записей.</span><span class="sxs-lookup"><span data-stu-id="c4583-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4583-114"><em>критерии</em></span><span class="sxs-lookup"><span data-stu-id="c4583-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="c4583-115">Выражение, определяющее, какие записи необходимо обновить.</span><span class="sxs-lookup"><span data-stu-id="c4583-115">An expression that determines which records will be updated.</span></span> <span data-ttu-id="c4583-116">Будут обновлены только те записи, которые удовлетворяют условиям выражения.</span><span class="sxs-lookup"><span data-stu-id="c4583-116">Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c4583-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4583-117">Remarks</span></span>

<span data-ttu-id="c4583-118">Инструкция UPDATE особенно полезна, когда необходимо изменить большое количество записей либо когда записи, которые необходимо изменить, находятся в нескольких таблицах.</span><span class="sxs-lookup"><span data-stu-id="c4583-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="c4583-119">Вы можете изменить одновременно несколько полей.</span><span class="sxs-lookup"><span data-stu-id="c4583-119">You can change several fields at the same time.</span></span> <span data-ttu-id="c4583-120">В следующем примере показано, как увеличить значения Order Amount на 10 процентов, а значения Freight на 3 процента для грузоотправителей в Соединенном Королевстве:</span><span class="sxs-lookup"><span data-stu-id="c4583-120">The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="c4583-121">Инструкция UPDATE не создает результирующее множество.</span><span class="sxs-lookup"><span data-stu-id="c4583-121">UPDATE does not generate a result set.</span></span> <span data-ttu-id="c4583-122">Кроме того, после обновления записи с помощью запроса на обновление вам не удастся отменить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="c4583-122">Also, after you update records using an update query, you cannot undo the operation.</span></span> <span data-ttu-id="c4583-123">Если вам необходимо узнать, какие записи были обновлены, сначала изучите результаты выполнения запроса на выборку, использующего те же критерии, а затем запустите запрос на обновление.</span><span class="sxs-lookup"><span data-stu-id="c4583-123">If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="c4583-124">Всегда храните резервные копии данных.</span><span class="sxs-lookup"><span data-stu-id="c4583-124">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="c4583-125">Если вы обновите не те записи, вы сможете восстановить их из резервных копий.</span><span class="sxs-lookup"><span data-stu-id="c4583-125">If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="c4583-126">Пример</span><span class="sxs-lookup"><span data-stu-id="c4583-126">Example</span></span>

<span data-ttu-id="c4583-127">В этом примере показано, как изменить значения в поле ReportsTo на 5 для всех записей сотрудников, у которых поле ReportsTo имеет значение 2.</span><span class="sxs-lookup"><span data-stu-id="c4583-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

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
