---
title: Index.Unique Property (DAO)
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
ms.openlocfilehash: bf2bbd8e1bf5c7c51d93e0669becbfd093e29994
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482469"
---
# <a name="indexunique-property-dao"></a><span data-ttu-id="656cc-102">Index.Unique Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="656cc-102">Index.Unique Property (DAO)</span></span>

<span data-ttu-id="656cc-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="656cc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="656cc-104">Задает или возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** уникальный индекс (основные) для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="656cc-104">Sets or returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="656cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="656cc-105">Syntax</span></span>

<span data-ttu-id="656cc-106">*выражение* . Уникальный</span><span class="sxs-lookup"><span data-stu-id="656cc-106">*expression* .Unique</span></span>

<span data-ttu-id="656cc-107">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="656cc-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="656cc-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="656cc-108">Remarks</span></span>

<span data-ttu-id="656cc-109">Значение этого свойства — чтение и запись, пока объект добавляется к коллекции, после чего он доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="656cc-109">This property setting is read/write until the object is appended to a collection, after which it's read-only.</span></span>

<span data-ttu-id="656cc-110">Уникальный индекс состоит из одного или нескольких полей, логически Упорядочить все записи в таблице в порядке уникальный, предварительно заданных.</span><span class="sxs-lookup"><span data-stu-id="656cc-110">A unique index consists of one or more fields that logically arrange all records in a table in a unique, predefined order.</span></span> <span data-ttu-id="656cc-111">Если индекс состоит из одного поля, значения в этом поле должно быть уникальным для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="656cc-111">If the index consists of one field, values in that field must be unique for the entire table.</span></span> <span data-ttu-id="656cc-112">Если индекс состоит из нескольких полей, в каждом поле может содержать повторяющиеся значения, но каждый сочетание значений из всех индексированных полей должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="656cc-112">If the index consists of more than one field, each field can contain duplicate values, but each combination of values from all the indexed fields must be unique.</span></span>

<span data-ttu-id="656cc-113">Если как **Уникальный** , так и **[основной](index-primary-property-dao.md)** **индекс** объекта задано значение **True**, индекс уникальное и основной: однозначно определяет все записи в таблице в порядке, предварительно определенные, логических.</span><span class="sxs-lookup"><span data-stu-id="656cc-113">If both the **Unique** and **[Primary](index-primary-property-dao.md)** properties of an **Index** object are set to **True**, the index is unique and primary: It uniquely identifies all records in the table in a predefined, logical order.</span></span> <span data-ttu-id="656cc-114">Если **основной** свойство имеет значение **False**, индекс находится вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="656cc-114">If the **Primary** property is set to **False**, the index is a secondary index.</span></span> <span data-ttu-id="656cc-115">Вторичные индексы (ключевые и неключевые) логически упорядочить записи в предопределенном порядке без служат в качестве идентификатора для записей в таблице.</span><span class="sxs-lookup"><span data-stu-id="656cc-115">Secondary indexes (both key and nonkey) logically arrange records in a predefined order without serving as an identifier for records in the table.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="656cc-116">У вас нет для создания индексов для таблиц, но в крупных, неиндексированные таблиц, доступ к определенной записи может уйти много времени.</span><span class="sxs-lookup"><span data-stu-id="656cc-116">You don't have to create indexes for tables, but in large, unindexed tables, accessing a specific record can take a long time.</span></span></P>
> <LI>
> <P><span data-ttu-id="656cc-117">Записей, полученных из таблицы без индексов возвращаются в определенной последовательности.</span><span class="sxs-lookup"><span data-stu-id="656cc-117">Records retrieved from tables without indexes are returned in no particular sequence.</span></span></P>
> <LI>
> <P><span data-ttu-id="656cc-118">Свойство <STRONG><A href="field-attributes-property-dao.md">атрибуты</A></STRONG> каждого объекта <STRONG><A href="field-object-dao.md">поля</A></STRONG> в объекте <STRONG>индекса</STRONG> определяет порядок записей и следовательно определяет методы доступа для этого объекта <STRONG>индекса</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="656cc-118">The <STRONG><A href="field-attributes-property-dao.md">Attributes</A></STRONG> property of each <STRONG><A href="field-object-dao.md">Field</A></STRONG> object in the <STRONG>Index</STRONG> object determines the order of records and consequently determines the access techniques to use for that <STRONG>Index</STRONG> object.</span></span></P>
> <LI>
> <P><span data-ttu-id="656cc-119">Уникальный индекс помогает оптимизировать поиск записей.</span><span class="sxs-lookup"><span data-stu-id="656cc-119">A unique index helps optimize finding records.</span></span></P>
> <LI>
> <P><span data-ttu-id="656cc-120">Индексы не влияют на физический порядок влияние индексов базовая таблица, как только записи обращением объекта <STRONG><A href="recordset-object-dao.md">набора записей</A></STRONG> в таблице тип при выборе определенного индекса или когда ядро базы данных Microsoft Access создает объекты <STRONG>набора записей</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="656cc-120">Indexes don't affect the physical order of a base table indexes affect only how the records are accessed by the table-type <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> object when a particular index is chosen or when the Microsoft Access database engine creates <STRONG>Recordset</STRONG> objects.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="656cc-121">Пример</span><span class="sxs-lookup"><span data-stu-id="656cc-121">Example</span></span>

<span data-ttu-id="656cc-122">В этом примере задается свойство **Уникальный** **индекс** объекта значение **True**и добавляет индекс коллекции **индексов** таблицы «Сотрудники».</span><span class="sxs-lookup"><span data-stu-id="656cc-122">This example sets the **Unique** property of a new **Index** object to **True**, and appends the Index to the **Indexes** collection of the Employees table.</span></span> <span data-ttu-id="656cc-123">Затем выполняется перечисление коллекции **индексов** **TableDef** и коллекции **свойств** каждого **индекса**.</span><span class="sxs-lookup"><span data-stu-id="656cc-123">It then enumerates the **Indexes** collection of the **TableDef** and the **Properties** collection of each **Index**.</span></span> <span data-ttu-id="656cc-124">Новый **индекс** только позволит одна запись с конкретной комбинации страны, LastName и FirstName в **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="656cc-124">The new **Index** will only allow one record with a particular combination of Country, LastName, and FirstName in the **TableDef**.</span></span>

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
