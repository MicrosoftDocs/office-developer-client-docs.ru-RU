---
title: Метод Recordset2. reQuery (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44f573d179c26677fc801dac82e0deecc3874fb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307212"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="b9c10-102">Метод Recordset2. reQuery (DAO)</span><span class="sxs-lookup"><span data-stu-id="b9c10-102">Recordset2.Requery method (DAO)</span></span>

<span data-ttu-id="b9c10-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9c10-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9c10-104">Обновляет данные в объекте **[Recordset](recordset-object-dao.md)** с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="b9c10-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9c10-105">Syntax</span></span>

<span data-ttu-id="b9c10-106">*Expression* . ReQuery (***невкуеридеф***)</span><span class="sxs-lookup"><span data-stu-id="b9c10-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="b9c10-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="b9c10-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9c10-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9c10-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9c10-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b9c10-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b9c10-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="b9c10-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b9c10-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b9c10-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b9c10-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b9c10-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9c10-113"><em>Невкуеридеф</em></span><span class="sxs-lookup"><span data-stu-id="b9c10-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="b9c10-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b9c10-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b9c10-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b9c10-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b9c10-116">Представляет значение свойства <strong>имени</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="b9c10-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b9c10-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9c10-117">Remarks</span></span>

<span data-ttu-id="b9c10-118">Используйте этот метод, чтобы убедиться, что объект **Recordset** содержит самые последние данные.</span><span class="sxs-lookup"><span data-stu-id="b9c10-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="b9c10-119">Этот метод повторно заполняет текущий **набор записей** с помощью текущих параметров запроса или (в рабочей области Microsoft Access) новыми, которые предоставляются аргументом невкуеридеф.</span><span class="sxs-lookup"><span data-stu-id="b9c10-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="b9c10-120">Если не указать аргумент невкуеридеф, то **набор записей** повторно заполняется в соответствии с тем же определением запроса и параметрами, которые использовались для первоначального заполнения объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9c10-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="b9c10-121">Все изменения базовых данных будут отражены во время этого повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="b9c10-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="b9c10-122">Если для создания объекта **Recordset**не использовался объект **QueryDef** , то **набор записей** повторно создается с нуля.</span><span class="sxs-lookup"><span data-stu-id="b9c10-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="b9c10-123">Если вы укажете исходный объект **QueryDef** в аргументе невкуеридеф, то этот **набор записей** будет повторно запрашиваться с использованием параметров, заданных объектом **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="b9c10-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="b9c10-124">Все изменения базовых данных будут отражены во время этого повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="b9c10-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="b9c10-125">Чтобы отразить любые изменения значений параметров запроса в наборе **записей**, необходимо указать аргумент невкуеридеф.</span><span class="sxs-lookup"><span data-stu-id="b9c10-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="b9c10-126">Если указать другой объект **QueryDef** , отличный от первоначально использованного для создания **набора записей**, то **набор записей** повторно создается с нуля.</span><span class="sxs-lookup"><span data-stu-id="b9c10-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="b9c10-127">При использовании **запроса Requery**первая запись в наборе **записей** становится текущей записью.</span><span class="sxs-lookup"><span data-stu-id="b9c10-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="b9c10-128">Невозможно использовать метод **restart** для объектов **Recordset** типа динамического подмножества или моментального снимка, для свойства restarted которого задано значение **false**. **[](recordset2-restartable-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="b9c10-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="b9c10-129">Однако при указании необязательного аргумента невкуеридеф свойство \*\*\*\* restarted игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b9c10-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="b9c10-130">Если параметры свойств **[BOF](recordset2-bof-property-dao.md)** и **[EOF](recordset2-eof-property-dao.md)** объекта **Recordset** имеют **значение true** после использования метода Requery, то \*\*\*\* запрос не возвращал какие бы то ни было записи, а объект **Recordset** не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="b9c10-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="b9c10-131">Пример</span><span class="sxs-lookup"><span data-stu-id="b9c10-131">Example</span></span>

<span data-ttu-id="b9c10-132">В этом примере показано, \*\*\*\* как можно использовать метод Requery для обновления запроса после изменения базовых данных.</span><span class="sxs-lookup"><span data-stu-id="b9c10-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b9c10-133">В этом примере показано, \*\*\*\* как можно использовать метод Requery для обновления запроса после изменения параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="b9c10-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```

