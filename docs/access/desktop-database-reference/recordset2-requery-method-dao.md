---
title: Метод Recordset2.Requery (DAO)
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
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="20635-102">Метод Recordset2.Requery (DAO)</span><span class="sxs-lookup"><span data-stu-id="20635-102">Recordset2.Requery method (DAO)</span></span>

<span data-ttu-id="20635-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20635-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20635-104">Обновляет данные в объекте **[Recordset](recordset-object-dao.md)** с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="20635-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="20635-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20635-105">Syntax</span></span>

<span data-ttu-id="20635-106">*выражение* .Requery(***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="20635-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="20635-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="20635-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="20635-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20635-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20635-109">Имя</span><span class="sxs-lookup"><span data-stu-id="20635-109">Name</span></span></p></th>
<th><p><span data-ttu-id="20635-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="20635-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="20635-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="20635-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="20635-112">Описание</span><span class="sxs-lookup"><span data-stu-id="20635-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20635-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="20635-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="20635-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="20635-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="20635-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="20635-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="20635-116">Представляет значение свойства <strong>Name</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="20635-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="20635-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="20635-117">Remarks</span></span>

<span data-ttu-id="20635-118">Используйте этот метод, чтобы обеспечить наличие самых последних данных в объекте **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="20635-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="20635-119">Этот метод повторно заполняет текущий объект **Recordset** с помощью текущих параметров запроса или (в рабочей области Microsoft Access) новыми параметрами, предоставляемыми аргументом newquerydef.</span><span class="sxs-lookup"><span data-stu-id="20635-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="20635-120">Если аргумент newquerydef не указан, объект **Recordset** повторно заполняется на основе того же определения запроса и параметров, использованных изначально для заполнения объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="20635-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="20635-121">Все изменения базовых данных будут отражены во время этого повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="20635-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="20635-122">Если вы не используете объект **QueryDef** для создания объекта **Recordset**, **Recordset** повторно создается с нуля.</span><span class="sxs-lookup"><span data-stu-id="20635-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="20635-123">Если в аргументе newquerydef указан исходный объект **QueryDef**, объект **Recordset** повторно запрашивается с помощью параметров, указанных объектом **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="20635-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="20635-124">Все изменения базовых данных будут отражены во время этого повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="20635-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="20635-125">Чтобы отразить любые изменения значений параметров запроса в объекте **Recordset**, необходимо указать аргумент newquerydef.</span><span class="sxs-lookup"><span data-stu-id="20635-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="20635-126">Если указать другой объект **QueryDef** вместо использованного изначально для создания объекта **Recordset**, **Recordset** повторно создается с нуля.</span><span class="sxs-lookup"><span data-stu-id="20635-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="20635-127">При использовании метода **Requery** первая запись в объекте **Recordset** становится текущей записью.</span><span class="sxs-lookup"><span data-stu-id="20635-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="20635-128">Вы не можете использовать метод **Requery** для объектов **Recordset** типа "Динамический набор" или "Статический набор", свойству **[Restartable](recordset2-restartable-property-dao.md)** которых присвоено значение **False**.</span><span class="sxs-lookup"><span data-stu-id="20635-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="20635-129">Но если указан необязательный аргумент newquerydef, свойство **Restartable** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="20635-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="20635-130">Если свойствам **[BOF](recordset2-bof-property-dao.md)** и **[EOF](recordset2-eof-property-dao.md)** объекта **Recordset** присвоено значение **True** после использования метода **Requery**, запрос не возвращает какие-либо записи и объект **Recordset** не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="20635-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="20635-131">Пример</span><span class="sxs-lookup"><span data-stu-id="20635-131">Example</span></span>

<span data-ttu-id="20635-132">В этом примере показано, как можно использовать метод **Requery** для обновления запроса после изменения базовых данных.</span><span class="sxs-lookup"><span data-stu-id="20635-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

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

<span data-ttu-id="20635-133">В этом примере показано, как можно использовать метод **Requery** для обновления запроса после изменения параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="20635-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

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

