---
title: DROP Statement (Microsoft Access SQL)
TOCTitle: DROP Statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fc43547d6b9b744e004d44fff14b3fe82360732
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481617"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="c2a54-102">DROP Statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c2a54-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c2a54-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2a54-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2a54-104">Удаление существующей таблицы, процедуры или представления из базы данных или удаление существующего индекса из таблицы.</span><span class="sxs-lookup"><span data-stu-id="c2a54-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="c2a54-105">Ядро СУБД Microsoft Access не поддерживает использование ПЕРЕТАСКИВАНИЯ или любой другой инструкции DDL с базами данных, ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="c2a54-105">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="c2a54-106">Используйте метод DAO **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="c2a54-106">Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a54-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2a54-107">Syntax</span></span>

<span data-ttu-id="c2a54-108">ПОМЕСТИТЕ {таблицы в *таблице* | Д *индекса* ИНДЕКСА *в таблице* | ПРОЦЕДУРА *процедуры* | Просмотр *представления*}</span><span class="sxs-lookup"><span data-stu-id="c2a54-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="c2a54-109">Инструкции DROP состоит из следующих частей:</span><span class="sxs-lookup"><span data-stu-id="c2a54-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2a54-110">Часть</span><span class="sxs-lookup"><span data-stu-id="c2a54-110">Part</span></span></p></th>
<th><p><span data-ttu-id="c2a54-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c2a54-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2a54-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="c2a54-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c2a54-113">Имя таблицы для удаления или таблицы, из которого удаляется индекс.</span><span class="sxs-lookup"><span data-stu-id="c2a54-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a54-114"><em>процедура</em></span><span class="sxs-lookup"><span data-stu-id="c2a54-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="c2a54-115">Имя процедуры, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c2a54-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a54-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="c2a54-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="c2a54-117">Имя представления для удаления.</span><span class="sxs-lookup"><span data-stu-id="c2a54-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a54-118"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="c2a54-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="c2a54-119">Имя индекса, удаляемый из <em>таблицы.</em></span><span class="sxs-lookup"><span data-stu-id="c2a54-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c2a54-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2a54-120">Remarks</span></span>

<span data-ttu-id="c2a54-121">Прежде чем удалить его или удаление индекса из его необходимо закрыть таблицы.</span><span class="sxs-lookup"><span data-stu-id="c2a54-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="c2a54-122">Можно также использовать [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) удаление индекса из таблицы.</span><span class="sxs-lookup"><span data-stu-id="c2a54-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="c2a54-123">[Создание таблицы](create-table-statement-microsoft-access-sql.md) можно использовать для создания таблицы и [CREATE INDEX](create-index-statement-microsoft-access-sql.md) или ALTER TABLE, чтобы создать индекс.</span><span class="sxs-lookup"><span data-stu-id="c2a54-123">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index.</span></span> <span data-ttu-id="c2a54-124">Для изменения таблицы, используйте ALTER TABLE.</span><span class="sxs-lookup"><span data-stu-id="c2a54-124">To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="c2a54-125">Пример</span><span class="sxs-lookup"><span data-stu-id="c2a54-125">Example</span></span>

<span data-ttu-id="c2a54-126">В следующем примере предполагается существование предполагаемую NewIndex индекса на таблице Employees базы данных Northwind.</span><span class="sxs-lookup"><span data-stu-id="c2a54-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="c2a54-127">В этом примере удаляется индекс MyIndex из таблицы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="c2a54-127">This example deletes the index MyIndex from the Employees table.</span></span>

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

<span data-ttu-id="c2a54-128">В этом примере удаляется таблицу Employees из базы данных.</span><span class="sxs-lookup"><span data-stu-id="c2a54-128">This example deletes the Employees table from the database.</span></span>

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
