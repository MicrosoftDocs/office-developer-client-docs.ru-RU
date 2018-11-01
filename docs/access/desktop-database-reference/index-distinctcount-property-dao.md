---
title: Index.DistinctCount Property (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2e609090e66a9bfd5b4b37d8e8e8a5546cc8469a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876892"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="2f258-102">Index.DistinctCount Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f258-102">Index.DistinctCount Property (DAO)</span></span>

<span data-ttu-id="2f258-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f258-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f258-104">Возвращает значение, указывающее количество уникальных значений для объекта **[индекса](index-object-dao.md)** , содержащихся в связанной таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2f258-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f258-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f258-105">Syntax</span></span>

<span data-ttu-id="2f258-106">*выражение* . Число различных значений</span><span class="sxs-lookup"><span data-stu-id="2f258-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="2f258-107">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="2f258-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f258-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f258-108">Remarks</span></span>

<span data-ttu-id="2f258-109">Проверьте свойства **число различных значений** , чтобы определить число уникальных значений или ключей в индекс.</span><span class="sxs-lookup"><span data-stu-id="2f258-109">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index.</span></span> <span data-ttu-id="2f258-110">Любую клавишу учитывается только один раз, даже если возможно наличие нескольких экземпляров данного значения Если индекс допускает дублирующиеся значения.</span><span class="sxs-lookup"><span data-stu-id="2f258-110">Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values.</span></span> <span data-ttu-id="2f258-111">Эта информация полезна в приложениях, которые пытаются оптимизировать доступ к данным, оценка данные индекса.</span><span class="sxs-lookup"><span data-stu-id="2f258-111">This information is useful in applications that attempt to optimize data access by evaluating index information.</span></span> <span data-ttu-id="2f258-112">Количество уникальных значений также называется количеством объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="2f258-112">The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="2f258-113">**Число различных значений** свойств всегда могут не отражать фактическое число разделов в конкретный момент времени.</span><span class="sxs-lookup"><span data-stu-id="2f258-113">The **DistinctCount** property won't always reflect the actual number of keys at a particular time.</span></span> <span data-ttu-id="2f258-114">Например, изменения, возникающие при отката обратная транзакций не будут отражены сразу же в **число различных значений** свойств.</span><span class="sxs-lookup"><span data-stu-id="2f258-114">For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property.</span></span> <span data-ttu-id="2f258-115">Значение свойства **число различных значений** также могут не отражать удаление записей с помощью уникальных ключей.</span><span class="sxs-lookup"><span data-stu-id="2f258-115">The **DistinctCount** property value also may not reflect the deletion of records with unique keys.</span></span> <span data-ttu-id="2f258-116">Номер будет точных сразу же после используйте метод **[CreateIndex](tabledef-createindex-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="2f258-116">The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="2f258-117">Пример</span><span class="sxs-lookup"><span data-stu-id="2f258-117">Example</span></span>

<span data-ttu-id="2f258-118">В этом примере используется свойство **число различных значений** для отображения как можно определить число уникальных значений в объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="2f258-118">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object.</span></span> <span data-ttu-id="2f258-119">Однако это значение — только точных сразу же после создания **индекса**.</span><span class="sxs-lookup"><span data-stu-id="2f258-119">However, this value is only accurate immediately after creating the **Index**.</span></span> <span data-ttu-id="2f258-120">Будут всегда точно, если ключи не изменять или добавляются новые ключи и старые ключи не удаляются; в противном случае оно не будет надежным.</span><span class="sxs-lookup"><span data-stu-id="2f258-120">It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable.</span></span> <span data-ttu-id="2f258-121">(Если эта процедура выполняется несколько раз, можно увидеть влияние на значения **число различных значений** свойств существующих объектов индекса.)</span><span class="sxs-lookup"><span data-stu-id="2f258-121">(If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
