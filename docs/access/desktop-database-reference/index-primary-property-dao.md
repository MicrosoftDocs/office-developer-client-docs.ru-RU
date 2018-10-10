---
title: Index.Primary Property (DAO)
TOCTitle: Primary Property
ms:assetid: 90eda1cb-cf7f-9682-9b74-81c27a37af16
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197416(v=office.15)
ms:contentKeyID: 48546336
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052908
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2d551b60919b1fb3d48c7ac75bbf7c6183aee04d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483284"
---
# <a name="indexprimary-property-dao"></a><span data-ttu-id="5c25f-102">Index.Primary Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="5c25f-102">Index.Primary Property (DAO)</span></span>


<span data-ttu-id="5c25f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c25f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="5c25f-104">Задает или возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** индекс первичного ключа для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5c25f-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a primary key index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c25f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c25f-105">Syntax</span></span>

<span data-ttu-id="5c25f-106">*выражение* . Основной</span><span class="sxs-lookup"><span data-stu-id="5c25f-106">*expression* .Primary</span></span>

<span data-ttu-id="5c25f-107">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="5c25f-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c25f-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c25f-108">Remarks</span></span>

<span data-ttu-id="5c25f-109">Значение свойства **основной** — чтение и запись для нового объекта **индекс** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **[индексов](indexes-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="5c25f-109">The **Primary** property setting is read/write for a new **Index** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span> <span data-ttu-id="5c25f-110">Если объект **[TableDef](tabledef-object-dao.md)** добавляется объект **индекса** , но объект **TableDef** не добавлено в коллекцию **[TableDefs](tabledefs-collection-dao.md)** , свойство **Index** — чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="5c25f-110">If the **Index** object is appended to the **[TableDef](tabledef-object-dao.md)** object but the **TableDef** object isn't appended to the **[TableDefs](tabledefs-collection-dao.md)** collection, the **Index** property is read/write.</span></span>

<span data-ttu-id="5c25f-111">Индекс первичного ключа состоит из одного или нескольких полей, которые однозначно идентифицируют все записи в таблице в предопределенном порядке.</span><span class="sxs-lookup"><span data-stu-id="5c25f-111">A primary key index consists of one or more fields that uniquely identify all records in a table in a predefined order.</span></span> <span data-ttu-id="5c25f-112">Так как поле индекса должно быть уникальным, свойство **[Уникальный](index-unique-property-dao.md)** **индекс** объекта имеет значение **True**.</span><span class="sxs-lookup"><span data-stu-id="5c25f-112">Because the index field must be unique, the **[Unique](index-unique-property-dao.md)** property of the **Index** object is set to **True**.</span></span> <span data-ttu-id="5c25f-113">Если индекс первичного ключа состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но каждый сочетание значений из всех индексированных полей должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="5c25f-113">If the primary key index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span> <span data-ttu-id="5c25f-114">Индекс первичного ключа состоит из ключа для таблицы и обычно содержит все поля первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="5c25f-114">A primary key index consists of a key for the table and usually contains the same fields as the primary key.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5c25f-115">У вас нет для создания индексов для таблиц, но в крупных, неиндексированные таблиц, доступ к определенной записи может уйти много времени.</span><span class="sxs-lookup"><span data-stu-id="5c25f-115">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span> <span data-ttu-id="5c25f-116">Свойство <STRONG><A href="field-attributes-property-dao.md">атрибуты</A></STRONG> каждого объекта <STRONG><A href="field-object-dao.md">поля</A></STRONG> в объекте <STRONG>индекса</STRONG> определяет порядок записей и следовательно определяет методы доступа для этого индекса.</span><span class="sxs-lookup"><span data-stu-id="5c25f-116">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that index.</span></span> <span data-ttu-id="5c25f-117">При создании новой таблицы в базе данных, рекомендуется создать индекс для одного или нескольких полей, которые однозначно идентифицируют каждую запись и задайте его свойство <STRONG>основного</STRONG> объекта <STRONG>индекса</STRONG> значение <STRONG>True</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="5c25f-117">When you create a new table in your database, it's a good idea to create an index on one or more fields that uniquely identify each record, and then set the <STRONG>Primary</STRONG> property of the <STRONG>Index</STRONG> object to <STRONG>True</STRONG>.</span></span></P>



<span data-ttu-id="5c25f-118">При установке первичный ключ для таблицы первичный ключ автоматически определяется как индекс первичного ключа для таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c25f-118">When you set a primary key for a table, the primary key is automatically defined as the primary key index for the table.</span></span>

## <a name="example"></a><span data-ttu-id="5c25f-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5c25f-119">Example</span></span>

<span data-ttu-id="5c25f-120">В этом примере **основной** используется для назначения нового **индекса** в новой **TableDef** в качестве основного **индекса** для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c25f-120">This example uses the **Primary** property to designate a new **Index** in a new **TableDef** as the primary **Index** for that table.</span></span> <span data-ttu-id="5c25f-121">Обратите внимание, что свойства **основной** значение **True,** автоматически задает **Уникальный** и **необходимые** свойства значение **True,** также.</span><span class="sxs-lookup"><span data-stu-id="5c25f-121">Note that setting the **Primary** property to **True** automatically sets **Unique** and **Required** properties to **True** as well.</span></span>

```vb
    Sub PrimaryX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim idxLoop As Index 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new TableDef object to the 
     ' TableDefs collection of the Northwind database. 
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTable") 
     tdfNew.Fields.Append tdfNew.CreateField("NumField", _ 
     dbLong, 20) 
     tdfNew.Fields.Append tdfNew.CreateField("TextField", _ 
     dbText, 20) 
     dbsNorthwind.TableDefs.Append tdfNew 
     
     With tdfNew 
     ' Create and append a new Index object to the 
     ' Indexes collection of the new TableDef object. 
     Set idxNew = .CreateIndex("NumIndex") 
     idxNew.Fields.Append idxNew.CreateField("NumField") 
     idxNew.Primary = True 
     .Indexes.Append idxNew 
     Set idxNew = .CreateIndex("TextIndex") 
     idxNew.Fields.Append idxNew.CreateField("TextField") 
     .Indexes.Append idxNew 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     
     With idxLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Fields collection of each Index 
     ' object. 
     Debug.Print " Fields" 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of each 
     ' Index object. 
     Debug.Print " Properties" 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & IIf(prpLoop = "", "[empty]", _ 
     prpLoop) 
     Next prpLoop 
     End With 
     
     Next idxLoop 
     
     End With 
     
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
