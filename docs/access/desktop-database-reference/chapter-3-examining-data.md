---
title: 'Глава 3: Проверка данных'
TOCTitle: 'Chapter 3: Examining data'
ms:assetid: 73c69134-3127-3344-d5c3-5ecb9e0e958b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249474(v=office.15)
ms:contentKeyID: 48545648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b489400536675fccced8f87aae515b019b87123
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936863"
---
# <a name="chapter-3-examining-data"></a><span data-ttu-id="e13f6-102">Глава 3: Проверка данных</span><span class="sxs-lookup"><span data-stu-id="e13f6-102">Chapter 3: Examining data</span></span>

<span data-ttu-id="e13f6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e13f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e13f6-104">Глава 2 объясняется порядок извлечения данных из источника данных в качестве объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e13f6-104">Chapter 2 explained how to retrieve data from a data source as a **Recordset** object.</span></span> <span data-ttu-id="e13f6-105">В этой главе рассматриваются **записей** более подробно, в том числе как перейти по **записей** и просматривать данные.</span><span class="sxs-lookup"><span data-stu-id="e13f6-105">This chapter will discuss the **Recordset** in more detail, including how to navigate through the **Recordset** and view its data.</span></span>

<span data-ttu-id="e13f6-106">**Наборы записей** имеют методы и свойства, предназначенные для упрощения их перемещение по ним и просматривать их содержимое.</span><span class="sxs-lookup"><span data-stu-id="e13f6-106">**Recordsets** have methods and properties designed to make it easy to move through them and examine their contents.</span></span> <span data-ttu-id="e13f6-107">В зависимости от функциональных возможностей, поддерживаемых поставщиком некоторые из **набора записей** методов и свойств не становятся доступны.</span><span class="sxs-lookup"><span data-stu-id="e13f6-107">Depending on the functionality supported by the provider, some **Recordset** methods or properties might not be available.</span></span> <span data-ttu-id="e13f6-108">Чтобы продолжить изучение объекта **набора записей** , рассмотрите **набора записей** , возвращаемого из образца базы данных Northwind на Microsoft SQL Server 2000, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="e13f6-108">To continue exploring the **Recordset** object, consider a **Recordset** that would be returned from the Northwind sample database on Microsoft SQL Server 2000, using the following code:</span></span>

```vb 
 
'BeginRsTour 
Public Sub RecordsetTour() 
 On Error GoTo ErrHandler: 
 
 Dim objRs As New ADODB.Recordset 
 Dim strSQL As String 
 
 strSQL = "SELECT ProductID, ProductName, UnitPrice FROM Products " & _ 
 "WHERE CategoryID = 7" '7 = Produce 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, _ 
 adLockReadOnly, adCmdText 
 
 'Clean up 
 objRs.Close 
 Set objRs = Nothing 
 Exit Sub 
 
ErrHandler: 
 If Not objRs Is Nothing Then 
 If objRs.State = adStateOpen Then objRs.Close 
 Set objRs = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndRsTour 
```

<br/>

<span data-ttu-id="e13f6-109">Этот запрос SQL возвращает **набора записей** с помощью пяти строк (записей) и три столбца (поля).</span><span class="sxs-lookup"><span data-stu-id="e13f6-109">This SQL query returns a **Recordset** with five rows (records) and three columns (fields).</span></span> <span data-ttu-id="e13f6-110">В следующей таблице показаны значения для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="e13f6-110">The values for each row are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e13f6-111">ПОЛЕ 0</span><span class="sxs-lookup"><span data-stu-id="e13f6-111">FIELD 0</span></span><br />
<span data-ttu-id="e13f6-112">Имя = ProductID</span><span class="sxs-lookup"><span data-stu-id="e13f6-112">Name = ProductID</span></span></p></th>
<th><p><span data-ttu-id="e13f6-113">ПОЛЕ 1</span><span class="sxs-lookup"><span data-stu-id="e13f6-113">FIELD 1</span></span><br />
<span data-ttu-id="e13f6-114">Имя = имя продукта</span><span class="sxs-lookup"><span data-stu-id="e13f6-114">Name = ProductName</span></span></p></th>
<th><p><span data-ttu-id="e13f6-115">ПОЛЕ 2</span><span class="sxs-lookup"><span data-stu-id="e13f6-115">FIELD 2</span></span><br />
<span data-ttu-id="e13f6-116">Имя = цена</span><span class="sxs-lookup"><span data-stu-id="e13f6-116">Name = UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e13f6-117">7</span><span class="sxs-lookup"><span data-stu-id="e13f6-117">7</span></span></p></td>
<td><p><span data-ttu-id="e13f6-118">Боб ячейку органических высохла Груши</span><span class="sxs-lookup"><span data-stu-id="e13f6-118">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="e13f6-119">30.0000</span><span class="sxs-lookup"><span data-stu-id="e13f6-119">30.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13f6-120">14</span><span class="sxs-lookup"><span data-stu-id="e13f6-120">14</span></span></p></td>
<td><p><span data-ttu-id="e13f6-121">Диаграмме</span><span class="sxs-lookup"><span data-stu-id="e13f6-121">Tofu</span></span></p></td>
<td><p><span data-ttu-id="e13f6-122">23.2500</span><span class="sxs-lookup"><span data-stu-id="e13f6-122">23.2500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13f6-123">28</span><span class="sxs-lookup"><span data-stu-id="e13f6-123">28</span></span></p></td>
<td><p><span data-ttu-id="e13f6-124">Квашеная капуста Rssle</span><span class="sxs-lookup"><span data-stu-id="e13f6-124">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="e13f6-125">45.6000</span><span class="sxs-lookup"><span data-stu-id="e13f6-125">45.6000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13f6-126">51</span><span class="sxs-lookup"><span data-stu-id="e13f6-126">51</span></span></p></td>
<td><p><span data-ttu-id="e13f6-127">Сушеные "apples"</span><span class="sxs-lookup"><span data-stu-id="e13f6-127">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="e13f6-128">53.0000</span><span class="sxs-lookup"><span data-stu-id="e13f6-128">53.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13f6-129">74</span><span class="sxs-lookup"><span data-stu-id="e13f6-129">74</span></span></p></td>
<td><p><span data-ttu-id="e13f6-130">Longlife диаграмме</span><span class="sxs-lookup"><span data-stu-id="e13f6-130">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="e13f6-131">10.0000</span><span class="sxs-lookup"><span data-stu-id="e13f6-131">10.0000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e13f6-132">Следующем разделе объясняется, как найти текущей позиции курсора в этом примере **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e13f6-132">The next section explains how to locate the current position of the cursor in this sample **Recordset**.</span></span>

<span data-ttu-id="e13f6-133">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="e13f6-133">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="e13f6-134">Поиск текущей записи (ADO)</span><span class="sxs-lookup"><span data-stu-id="e13f6-134">Locating the current record (ADO)</span></span>](locating-the-current-record.md)
- [<span data-ttu-id="e13f6-135">Переход между данными (ADO)</span><span class="sxs-lookup"><span data-stu-id="e13f6-135">Navigating through the data (ADO)</span></span>](navigating-through-the-data.md)
- [<span data-ttu-id="e13f6-136">Общие сведения о структуре набора записей (ADO)</span><span class="sxs-lookup"><span data-stu-id="e13f6-136">Understanding Recordset structure (ADO)</span></span>](understanding-recordset-structure.md)