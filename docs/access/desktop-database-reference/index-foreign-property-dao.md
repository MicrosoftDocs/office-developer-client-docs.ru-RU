---
title: Свойство index. Foreign (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291819"
---
# <a name="indexforeign-property-dao"></a><span data-ttu-id="2989b-102">Свойство index. Foreign (DAO)</span><span class="sxs-lookup"><span data-stu-id="2989b-102">Index.Foreign property (DAO)</span></span>

<span data-ttu-id="2989b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2989b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2989b-104">Возвращает значение, которое указывает, представляет ли объект **[index](index-object-dao.md)** внешний ключ в таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2989b-104">Returns a value that indicates whether an **[Index](index-object-dao.md)** object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2989b-105">.</span><span class="sxs-lookup"><span data-stu-id="2989b-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="2989b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2989b-106">Syntax</span></span>

<span data-ttu-id="2989b-107">*Expression* . Правительства</span><span class="sxs-lookup"><span data-stu-id="2989b-107">*expression* .Foreign</span></span>

<span data-ttu-id="2989b-108">*Expression (выражение* ) Переменная, представляющая объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="2989b-108">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2989b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="2989b-109">Remarks</span></span>

<span data-ttu-id="2989b-110">Возвращаемое значение — это **логический** тип данных, который возвращает **значение true** , если объект **index** представляет внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="2989b-110">The return value is a **Boolean** data type that returns **True** if the **Index** object represents a foreign key.</span></span>

<span data-ttu-id="2989b-111">Внешний ключ состоит из одного или нескольких полей в иностранной таблице, которые уникально идентифицируют все строки в главной таблице.</span><span class="sxs-lookup"><span data-stu-id="2989b-111">A foreign key consists of one or more fields in a foreign table that uniquely identify all rows in a primary table.</span></span>

<span data-ttu-id="2989b-112">Ядро СУБД Microsoft Access создает объект **индекса** для внешней таблицы и задает **внешнее** свойство при создании связи, которая обеспечивает целостность ссылок.</span><span class="sxs-lookup"><span data-stu-id="2989b-112">The Microsoft Access database engine creates an **Index** object for the foreign table and sets the **Foreign** property when you create a relationship that enforces referential integrity.</span></span>

## <a name="example"></a><span data-ttu-id="2989b-113">Пример</span><span class="sxs-lookup"><span data-stu-id="2989b-113">Example</span></span>

<span data-ttu-id="2989b-114">В этом примере показано, как **внешнее** свойство может указывать, какие объекты **индекса** **tabledef** являются индексами внешних ключей.</span><span class="sxs-lookup"><span data-stu-id="2989b-114">This example shows how the **Foreign** property can indicate which **Index** objects in a **TableDef** are foreign key indexes.</span></span> <span data-ttu-id="2989b-115">Такие индексы создаются ядром СУБД Microsoft Access при создании **отношения** .</span><span class="sxs-lookup"><span data-stu-id="2989b-115">Such indexes are created by the Microsoft Access database engine when a **Relation** is created.</span></span> <span data-ttu-id="2989b-116">По умолчанию для индексов внешних ключей используется имя основной таблицы и имя внешней таблицы.</span><span class="sxs-lookup"><span data-stu-id="2989b-116">The default name for the foreign key indexes is the name of the primary table plus the name of the foreign table.</span></span> <span data-ttu-id="2989b-117">Для выполнения этой процедуры требуется функция Фореигнаутпут.</span><span class="sxs-lookup"><span data-stu-id="2989b-117">The ForeignOutput function is required for this procedure to run.</span></span>

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
