---
title: Свойство Field2.Required (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292722"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="068fd-102">Свойство Field2.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="068fd-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="068fd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="068fd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="068fd-104">Задает или возвращает значение, которое указывает, требуется ли **объекту Field2** значение non-Null.</span><span class="sxs-lookup"><span data-stu-id="068fd-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="068fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="068fd-105">Syntax</span></span>

<span data-ttu-id="068fd-106">*выражения* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="068fd-106">*expression* .Required</span></span>

<span data-ttu-id="068fd-107">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="068fd-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="068fd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="068fd-108">Remarks</span></span>

<span data-ttu-id="068fd-109">Для **поля 2,** еще не примыкаемого к коллекции **Fields,** это свойство является чтением и написанием.</span><span class="sxs-lookup"><span data-stu-id="068fd-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="068fd-110">Доступность **требуемого** свойства зависит от объекта, который содержит коллекцию **[Полей,](fields-collection-dao.md)** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="068fd-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="068fd-111">Если коллекция Fields принадлежит</span><span class="sxs-lookup"><span data-stu-id="068fd-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="068fd-112">Затем требуется</span><span class="sxs-lookup"><span data-stu-id="068fd-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="068fd-113">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="068fd-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="068fd-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="068fd-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fd-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="068fd-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="068fd-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="068fd-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fd-117">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="068fd-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="068fd-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="068fd-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="068fd-119">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="068fd-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="068fd-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="068fd-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="068fd-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="068fd-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="068fd-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="068fd-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="068fd-123">Необходимое свойство  можно использовать вместе с свойством **AllowZeroLength,** **ValidateOnSet** или **ValidationRule** для определения действительности параметра свойства **Value** для этого объекта **Field2.**</span><span class="sxs-lookup"><span data-stu-id="068fd-123">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object.</span></span> <span data-ttu-id="068fd-124">Если  необходимое свойство задано **false,** поле может содержать значения **null,** а также значения, которые соответствуют условиям, указанным в параметрах **свойств AllowZeroLength** и **ValidationRule.**</span><span class="sxs-lookup"><span data-stu-id="068fd-124">If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="068fd-125">Если вы можете установить это свойство для объекта **Index** или **объекта Field2,** установите его для **объекта Field2.**</span><span class="sxs-lookup"><span data-stu-id="068fd-125">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object.</span></span> <span data-ttu-id="068fd-126">Достоверность параметра свойства объекта **Field2** проверяется до проверки объекта **Index.**</span><span class="sxs-lookup"><span data-stu-id="068fd-126">The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="068fd-127">Пример</span><span class="sxs-lookup"><span data-stu-id="068fd-127">Example</span></span>

<span data-ttu-id="068fd-128">В этом примере используется свойство **Required** для отчета о том, какие поля в трех разных таблицах должны содержать данные, чтобы добавить новую запись.</span><span class="sxs-lookup"><span data-stu-id="068fd-128">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added.</span></span> <span data-ttu-id="068fd-129">Для запуска этой процедуры требуется процедура RequiredOutput.</span><span class="sxs-lookup"><span data-stu-id="068fd-129">The RequiredOutput procedure is required for this procedure to run.</span></span>

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

