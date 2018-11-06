---
title: Метод Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5c98eeb94e49693cf13d358987307f61f15069c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998338"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="1ec5f-102">Метод Recordset.Requery (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ec5f-102">Recordset.Requery method (DAO)</span></span>

<span data-ttu-id="1ec5f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ec5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ec5f-104">Обновляет данные в объект **[набора записей](recordset-object-dao.md)** , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec5f-105">Syntax</span></span>

<span data-ttu-id="1ec5f-106">*выражение* . Обновление (***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="1ec5f-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="1ec5f-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1ec5f-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ec5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec5f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ec5f-109">Имя</span><span class="sxs-lookup"><span data-stu-id="1ec5f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="1ec5f-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="1ec5f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="1ec5f-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1ec5f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="1ec5f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="1ec5f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ec5f-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="1ec5f-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="1ec5f-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1ec5f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="1ec5f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1ec5f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1ec5f-116">Представляет значение свойства <strong>Name</strong> объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="1ec5f-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1ec5f-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="1ec5f-117">Remarks</span></span>

<span data-ttu-id="1ec5f-118">Используйте этот метод, чтобы убедиться в том, что **набор записей** содержит последние данные.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="1ec5f-119">Этот метод повторно заполняет текущего **набора записей** с помощью любого из текущего запроса или (в рабочей области для Microsoft Access) новых структур указано в аргументе newquerydef.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="1ec5f-120">Если не указан аргумент newquerydef, **записей** повторно заполняется на основе одного определения запроса и параметры, используемые для заполнения изначально **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="1ec5f-121">Любые изменения в базовые данные будут отражены во время повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="1ec5f-122">Если **QueryDef** не используется для создания **записей**, **записей** повторно создать с нуля.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="1ec5f-123">При указании исходного **QueryDef** в аргументе newquerydef, затем **записей** обновляется с использованием параметров, указанного идентификатором **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="1ec5f-124">Любые изменения в базовые данные будут отражены во время повторного заполнения.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="1ec5f-125">Чтобы отразить любые изменения значения параметров запроса в **набор записей**, необходимо указать аргумент newquerydef.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="1ec5f-126">Если указать другой **QueryDef** чем что использовалась для создания **записей** **набора записей** повторно создать с нуля.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="1ec5f-127">При использовании **повторный запрос**первой записи в **набор записей** становится текущей.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="1ec5f-128">Нельзя использовать метод **повторный запрос** на или моментальный снимок добавляющий объектов **наборов записей** , свойство **[Restartable](recordset-restartable-property-dao.md)** имеет значение **False**.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="1ec5f-129">Тем не менее если вы задаете newquerydef необязательный аргумент, свойство **Restartable** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="1ec5f-130">Если **как **[BOF](recordset-bof-property-dao.md)** , так и параметры свойства **[EOF](recordset-eof-property-dao.md)** объекта **набора записей** выполняются после использования метода **повторный запрос** ,** запрос не возвращает никаких записей и **записей** не содержит данных.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-130">If both the **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="1ec5f-131">Пример</span><span class="sxs-lookup"><span data-stu-id="1ec5f-131">Example</span></span>

<span data-ttu-id="1ec5f-132">В этом примере показано использование метода **повторный запрос** для обновления запроса после изменения базовых данных.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
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

<span data-ttu-id="1ec5f-133">В этом примере показано использование метода **повторный запрос** для обновления запроса после изменения параметров запроса.</span><span class="sxs-lookup"><span data-stu-id="1ec5f-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
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

