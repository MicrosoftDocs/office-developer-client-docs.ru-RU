---
title: Свойство Index.Foreign (DAO)
TOCTitle: Foreign Property
ms:assetid: 81272436-a506-4b72-fd28-2d68e76d6d9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196489(v=office.15)
ms:contentKeyID: 48545943
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052974
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a3c6adfaf9648147a763f997ce2a91aadc4f7637
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707194"
---
# <a name="indexforeign-property-dao"></a><span data-ttu-id="9b93c-102">Свойство Index.Foreign (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b93c-102">Index.Foreign property (DAO)</span></span>

<span data-ttu-id="9b93c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b93c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b93c-104">Возвращает значение, указывающее, представляет ли объект **[индекса](index-object-dao.md)** внешний ключ в таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9b93c-104">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="9b93c-105">.</span><span class="sxs-lookup"><span data-stu-id="9b93c-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="9b93c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b93c-106">Syntax</span></span>

<span data-ttu-id="9b93c-107">*выражение* . Внешний</span><span class="sxs-lookup"><span data-stu-id="9b93c-107">*expression* .Foreign</span></span>

<span data-ttu-id="9b93c-108">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="9b93c-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b93c-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b93c-109">Remarks</span></span>

<span data-ttu-id="9b93c-110">Возвращаемое значение имеет тип данных **Boolean** , которое возвращает **значение True,** Если объект **индекса** представляет внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="9b93c-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="9b93c-111">Внешний ключ состоит из одного или нескольких полей внешней таблицы, которые однозначно идентифицируют все строки в основной таблице.</span><span class="sxs-lookup"><span data-stu-id="9b93c-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="9b93c-112">Ядро базы данных Microsoft Access создает объект **индекса** для таблицы внешнего и задает свойство **внешнего** при создании отношения, которое обеспечивает целостность данных.</span><span class="sxs-lookup"><span data-stu-id="9b93c-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="9b93c-113">Пример</span><span class="sxs-lookup"><span data-stu-id="9b93c-113">Example</span></span>

<span data-ttu-id="9b93c-114">В этом примере показано, как свойство **внешнего** позволяет определить, какие объекты **индекса** **TableDef** внешнего ключа индексов.</span><span class="sxs-lookup"><span data-stu-id="9b93c-114">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes.</span></span> <span data-ttu-id="9b93c-115">Такие индексы создаются ядром СУБД Microsoft Access, при создании **отношения** .</span><span class="sxs-lookup"><span data-stu-id="9b93c-115">Such indexes are created by the Microsoft Access database engine when a **Relation** is created.</span></span> <span data-ttu-id="9b93c-116">Имя по умолчанию для внешнего ключа индексов — это имя основной таблицы, а также имя внешней таблицы.</span><span class="sxs-lookup"><span data-stu-id="9b93c-116">The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table.</span></span> <span data-ttu-id="9b93c-117">Функция ForeignOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9b93c-117">The ForeignOutput function is required for this procedure to run.</span></span>

```vb
    Sub ForeignX() 
     
     Dim dbsNorthwind As Database 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Print report on foreign key indexes from two 
     ' TableDef objects and a QueryDef object. 
     ForeignOutput .TableDefs!Products 
     ForeignOutput .TableDefs!Orders 
     ForeignOutput .TableDefs![Order Details] 
     
     .Close 
     End With 
     
    End Sub 
     
    Function ForeignOutput(tdfTemp As TableDef) 
     
     Dim idxLoop As Index 
     
     With tdfTemp 
     Debug.Print "Indexes in " & .Name & " TableDef" 
     ' Enumerate the Indexes collection of the specified 
     ' TableDef object. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Debug.Print " Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     End With 
     
    End Function
```
