---
title: Свойство Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf5e459773cd0fa0976704834b1b73467fc75294
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937409"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="78252-102">Свойство Field2.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="78252-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="78252-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="78252-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="78252-104">Задает или возвращает значение, которое указывает, требуется ли объект **поле2** ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="78252-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="78252-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78252-105">Syntax</span></span>

<span data-ttu-id="78252-106">*выражение* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="78252-106">*expression* .Required</span></span>

<span data-ttu-id="78252-107">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="78252-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="78252-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="78252-108">Remarks</span></span>

<span data-ttu-id="78252-109">Для **поле2** еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="78252-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="78252-110">Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию **[полей](fields-collection-dao.md)** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="78252-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="78252-111">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="78252-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="78252-112">Затем необходимо — это</span><span class="sxs-lookup"><span data-stu-id="78252-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78252-113">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="78252-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="78252-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78252-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78252-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="78252-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="78252-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78252-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78252-117">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="78252-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="78252-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78252-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78252-119"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="78252-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="78252-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78252-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78252-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="78252-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="78252-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="78252-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78252-123">Свойства **необходимые** вместе со свойством **пустые строки**, **Проверка набора**или **значение** можно использовать для определения действительности параметр свойства **Value** объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="78252-123">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object.</span></span> <span data-ttu-id="78252-124">Если **требуется** свойство имеет значение **False**, поле может содержать значения **null** , а также значения, которые соответствуют условиям, указанным в параметрах свойство **пустые строки** и **значение** .</span><span class="sxs-lookup"><span data-stu-id="78252-124">If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="78252-125">При установке этого свойства для объекта **индекса** или объект **поле2** устанавливалось для объекта **поле2** .</span><span class="sxs-lookup"><span data-stu-id="78252-125">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object.</span></span> <span data-ttu-id="78252-126">Действия значение свойства для объекта **поле2** проверяется до этого объекта **индекса** .</span><span class="sxs-lookup"><span data-stu-id="78252-126">The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="78252-127">Пример</span><span class="sxs-lookup"><span data-stu-id="78252-127">Example</span></span>

<span data-ttu-id="78252-128">В этом примере используется свойство **требуется** отчет о котором поля в три различных таблицы должен содержать данные в порядке для новой записи для добавления.</span><span class="sxs-lookup"><span data-stu-id="78252-128">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added.</span></span> <span data-ttu-id="78252-129">Процедура RequiredOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="78252-129">The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

