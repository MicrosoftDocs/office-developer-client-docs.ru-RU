---
title: Свойство index. Дистинкткаунт (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 3264ea010db12f3fee6c16bd82fb19ed9bda1992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291847"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="fef1d-102">Свойство index. Дистинкткаунт (DAO)</span><span class="sxs-lookup"><span data-stu-id="fef1d-102">Index.DistinctCount property (DAO)</span></span>

<span data-ttu-id="fef1d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fef1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fef1d-104">Возвращает значение, которое указывает количество уникальных значений для объекта **[index](index-object-dao.md)** , включенных в связанную таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fef1d-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fef1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fef1d-105">Syntax</span></span>

<span data-ttu-id="fef1d-106">*Expression* . Дистинкткаунт</span><span class="sxs-lookup"><span data-stu-id="fef1d-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="fef1d-107">*Expression (выражение* ) Переменная, представляющая объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="fef1d-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fef1d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="fef1d-108">Remarks</span></span>

<span data-ttu-id="fef1d-109">Проверьте свойство **дистинкткаунт** , чтобы определить количество уникальных значений или ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="fef1d-109">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index.</span></span> <span data-ttu-id="fef1d-110">Любой ключ подсчитывается только один раз, несмотря на то, что в индексе допускаются повторяющиеся значения.</span><span class="sxs-lookup"><span data-stu-id="fef1d-110">Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values.</span></span> <span data-ttu-id="fef1d-111">Эта информация полезна в приложениях, которые пытаются оптимизировать доступ к данным, оценивая сведения об индексах.</span><span class="sxs-lookup"><span data-stu-id="fef1d-111">This information is useful in applications that attempt to optimize data access by evaluating index information.</span></span> <span data-ttu-id="fef1d-112">Количество уникальных значений также называется количеством объектов **индекса** .</span><span class="sxs-lookup"><span data-stu-id="fef1d-112">The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="fef1d-113">Свойство **дистинкткаунт** не всегда отражает фактическое число ключей в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="fef1d-113">The **DistinctCount** property won't always reflect the actual number of keys at a particular time.</span></span> <span data-ttu-id="fef1d-114">Например, изменение, вызванное выполненной откатной транзакцией, не будет немедленно отражено в свойстве **дистинкткаунт** .</span><span class="sxs-lookup"><span data-stu-id="fef1d-114">For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property.</span></span> <span data-ttu-id="fef1d-115">Значение свойства **дистинкткаунт** также может не отражать удаление записей с уникальными ключами.</span><span class="sxs-lookup"><span data-stu-id="fef1d-115">The **DistinctCount** property value also may not reflect the deletion of records with unique keys.</span></span> <span data-ttu-id="fef1d-116">После использования метода **[креатеиндекс](tabledef-createindex-method-dao.md)** число будет точным.</span><span class="sxs-lookup"><span data-stu-id="fef1d-116">The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="fef1d-117">Пример</span><span class="sxs-lookup"><span data-stu-id="fef1d-117">Example</span></span>

<span data-ttu-id="fef1d-118">В этом примере используется свойство **дистинкткаунт** , чтобы показать, как можно определить количество уникальных значений в объекте **index** .</span><span class="sxs-lookup"><span data-stu-id="fef1d-118">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object.</span></span> <span data-ttu-id="fef1d-119">Однако это значение является точным только сразу после создания **индекса**.</span><span class="sxs-lookup"><span data-stu-id="fef1d-119">However, this value is only accurate immediately after creating the **Index**.</span></span> <span data-ttu-id="fef1d-120">Он останется точным, если ключи не изменятся или добавляются новые ключи, а старые ключи не удаляются. в противном случае он не будет надежным.</span><span class="sxs-lookup"><span data-stu-id="fef1d-120">It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable.</span></span> <span data-ttu-id="fef1d-121">(Если эта процедура выполняется несколько раз, вы можете увидеть, как влияют значения свойства **дистинкткаунт** существующих объектов index.)</span><span class="sxs-lookup"><span data-stu-id="fef1d-121">(If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
