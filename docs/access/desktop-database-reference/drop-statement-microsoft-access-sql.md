---
title: Инструкция DROP (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718296"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="117e8-102">Инструкция DROP (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="117e8-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="117e8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="117e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="117e8-104">Удаляет существующую таблицу, процедуру или представление из базы данных либо удаляет существующий индекс из таблицы.</span><span class="sxs-lookup"><span data-stu-id="117e8-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="117e8-105">Ядро СУБД Microsoft Access не поддерживает использование инструкции DROP или любых инструкций DDL с базами данных с ядрами СУБД, отличными от Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="117e8-105">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="117e8-106">Вместо этого используйте метод DAO **Delete**.</span><span class="sxs-lookup"><span data-stu-id="117e8-106">Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="117e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="117e8-107">Syntax</span></span>

<span data-ttu-id="117e8-108">DROP {TABLE *таблица* | INDEX *индекс* ON *таблица* | PROCEDURE *процедура* | VIEW *представление*}</span><span class="sxs-lookup"><span data-stu-id="117e8-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="117e8-109">Инструкция DROP состоит из трех указанных ниже частей.</span><span class="sxs-lookup"><span data-stu-id="117e8-109">The Put statement syntax has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="117e8-110">Часть</span><span class="sxs-lookup"><span data-stu-id="117e8-110">Part</span></span></p></th>
<th><p><span data-ttu-id="117e8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="117e8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="117e8-112"><em>таблица</em></span><span class="sxs-lookup"><span data-stu-id="117e8-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="117e8-113">Имя таблицы, которую необходимо удалить, либо таблицы, из которой необходимо удалить индекс.</span><span class="sxs-lookup"><span data-stu-id="117e8-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="117e8-114"><em>процедура</em></span><span class="sxs-lookup"><span data-stu-id="117e8-114"><em>Procedure</em></span></span></p></td>
<td><p><span data-ttu-id="117e8-115">Имя процедуры, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="117e8-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="117e8-116"><em>представление</em></span><span class="sxs-lookup"><span data-stu-id="117e8-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="117e8-117">Имя представления, которое необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="117e8-117">The name of the view to switch to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="117e8-118"><em>индекс</em></span><span class="sxs-lookup"><span data-stu-id="117e8-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="117e8-119">Имя индекса, который необходимо удалить из <em>таблицы</em>.</span><span class="sxs-lookup"><span data-stu-id="117e8-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="117e8-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="117e8-120">Remarks</span></span>

<span data-ttu-id="117e8-121">Чтобы можно было удалить таблицу или индекс из нее, необходимо сначала закрыть эту таблицу.</span><span class="sxs-lookup"><span data-stu-id="117e8-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="117e8-122">Кроме того, для удаления индекса из таблицы можно использовать инструкцию [ALTER TABLE](alter-table-statement-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="117e8-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="117e8-123">С помощью инструкции [CREATE TABLE](create-table-statement-microsoft-access-sql.md) можно создать таблицу, а с помощью инструкции [CREATE INDEX](create-index-statement-microsoft-access-sql.md) или ALTER TABLE — создать индекс.</span><span class="sxs-lookup"><span data-stu-id="117e8-123">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index.</span></span> <span data-ttu-id="117e8-124">Изменить таблицу можно с помощью инструкции ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="117e8-124">To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="117e8-125">Пример</span><span class="sxs-lookup"><span data-stu-id="117e8-125">Example</span></span>

<span data-ttu-id="117e8-126">В примере ниже предполагается, что существует гипотетический индекс NewIndex в таблице Employees в базе данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="117e8-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="117e8-127">В этом примере показано, как удалить индекс MyIndex из таблицы Employees.</span><span class="sxs-lookup"><span data-stu-id="117e8-127">This example deletes the index MyIndex from the Employees table.</span></span>

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="117e8-128">В этом примере показано, как удалить таблицу Employees из базы данных.</span><span class="sxs-lookup"><span data-stu-id="117e8-128">This example deletes the Employees table from the database.</span></span>

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
