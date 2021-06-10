---
title: Свойство Index.Unique (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291694"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="7fa3b-102">Свойство Index.Unique (DAO)</span><span class="sxs-lookup"><span data-stu-id="7fa3b-102">Index.Unique property (DAO)</span></span>

<span data-ttu-id="7fa3b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fa3b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fa3b-104">Задает или возвращает значение, которое указывает, представляет ли объект **[Index](index-object-dao.md)** уникальный (ключевой) индекс для таблицы (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7fa3b-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fa3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fa3b-105">Syntax</span></span>

<span data-ttu-id="7fa3b-106">*выражения* . Уникальный</span><span class="sxs-lookup"><span data-stu-id="7fa3b-106">*expression* .Unique</span></span>

<span data-ttu-id="7fa3b-107">*выражение* Переменная, представляюная объект **Index.**</span><span class="sxs-lookup"><span data-stu-id="7fa3b-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fa3b-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7fa3b-108">Remarks</span></span>

<span data-ttu-id="7fa3b-109">Этот параметр свойства считыв или записывай до тех пор, пока объект не будет примыкать к коллекции, после чего он будет только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="7fa3b-110">Уникальный индекс состоит из одного или нескольких полей, логически упорядочив все записи в таблице в уникальном заранее определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-110">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order.</span></span> <span data-ttu-id="7fa3b-111">Если индекс состоит из одного поля, значения в этом поле должны быть уникальными для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-111">If the index consists of one field, values in that field must be unique for the entire table.</span></span> <span data-ttu-id="7fa3b-112">Если индекс состоит из нескольких полей, каждое поле может содержать дублирующие значения, но каждая комбинация значений из всех проиндексированные поля должна быть уникальной.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-112">If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="7fa3b-113">Если уникальные **[](index-primary-property-dao.md)** и первичные свойства объекта **Index** задают  **true,** индекс является уникальным и первичным: он однозначно определяет все записи в таблице в заранее определенном логическом порядке.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-113">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order.</span></span> <span data-ttu-id="7fa3b-114">Если свойство **Primary** настроено на **False,** индекс является вторичным индексом.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-114">If the **Primary** property is set to **False**, the index is a secondary index.</span></span> <span data-ttu-id="7fa3b-115">Вторичные индексы (как ключевые, так и неконкретные) логически упорядочивали записи в заранее заранее определенном порядке без использования в качестве идентификатора для записей в таблице.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-115">Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>

> [!NOTE]
> - <span data-ttu-id="7fa3b-116">Вам не нужно создавать индексы для таблиц, но в больших, неиндексуальных таблицах доступ к определенной записи может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span>
> - <span data-ttu-id="7fa3b-117">Записи, извлеченные из таблиц без индексов, возвращаются без определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span>
> - <span data-ttu-id="7fa3b-118">Свойство **[Атрибуты](field-attributes-property-dao.md)** каждого объекта **[Field](field-object-dao.md)** в объекте **Index** определяет порядок записей и, следовательно, определяет методы доступа, которые необходимо использовать для этого **объекта Index.**</span><span class="sxs-lookup"><span data-stu-id="7fa3b-118">The **[Attributes](field-attributes-property-dao.md)** property of each **[Field](field-object-dao.md)** object in the **Index** object determines the order of records and consequently determines the access techniques to use for that **Index** object.</span></span>
> - <span data-ttu-id="7fa3b-119">Уникальный индекс помогает оптимизировать поиск записей.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-119">A unique index helps optimize finding records.</span></span>
> - <span data-ttu-id="7fa3b-120">Индексы не влияют на физический порядок базовой таблицы; Индексы влияют только на то, как записи доступны объекту **[Recordset](recordset-object-dao.md)** в таблице, когда выбран определенный индекс или когда в движке базы данных Microsoft Access создаются объекты **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="7fa3b-120">Indexes don't affect the physical order of a base table; indexes affect only how the records are accessed by the table-type **[Recordset](recordset-object-dao.md)** object when a particular index is chosen or when the Microsoft Access database engine creates **Recordset** objects.</span></span>

## <a name="example"></a><span data-ttu-id="7fa3b-121">Пример</span><span class="sxs-lookup"><span data-stu-id="7fa3b-121">Example</span></span>

<span data-ttu-id="7fa3b-122">В этом примере **уникальное** свойство нового объекта **Index** определяется как **True** и придает индекс коллекции **Indexes** таблицы Employees.</span><span class="sxs-lookup"><span data-stu-id="7fa3b-122">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table.</span></span> <span data-ttu-id="7fa3b-123">Далее в нем огосвидетельна коллекция **Индексов** **TableDef** и коллекция **свойств** каждого **индекса.**</span><span class="sxs-lookup"><span data-stu-id="7fa3b-123">It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**.</span></span> <span data-ttu-id="7fa3b-124">Новый индекс **разрешает** только одну запись с определенной комбинацией Country, LastName и FirstName в **TableDef.**</span><span class="sxs-lookup"><span data-stu-id="7fa3b-124">The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
