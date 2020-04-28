---
title: Свойство Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52900d4a60002695866b9960fb6b80cefeb2b2ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292981"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="3b32f-102">Свойство Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b32f-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="3b32f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b32f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b32f-104">Задает или возвращает значение, которое указывает, требуется ли для объекта **[field](field-object-dao.md)** значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="3b32f-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b32f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b32f-105">Syntax</span></span>

<span data-ttu-id="3b32f-106">*Expression* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="3b32f-106">*expression* .Required</span></span>

<span data-ttu-id="3b32f-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="3b32f-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b32f-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b32f-108">Remarks</span></span>

<span data-ttu-id="3b32f-109">Для **поля** , еще не добавленного в коллекцию **Fields** , это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3b32f-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="3b32f-110">Доступность **обязательного** свойства зависит от объекта, содержащего коллекцию [Fields](fields-collection-dao.md) , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3b32f-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b32f-111">Если коллекция Fields принадлежит к элементу</span><span class="sxs-lookup"><span data-stu-id="3b32f-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="3b32f-112">Затем необходимо</span><span class="sxs-lookup"><span data-stu-id="3b32f-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b32f-113">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3b32f-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b32f-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3b32f-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b32f-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3b32f-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b32f-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32f-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b32f-117">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3b32f-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b32f-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b32f-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b32f-119">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="3b32f-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b32f-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3b32f-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b32f-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3b32f-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="3b32f-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b32f-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3b32f-123">Свойство **Required** , Валидатеонсет или ValidationRule можно использовать вместе со свойством **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** или **[ValidationRule](field-validationrule-property-dao.md)** , чтобы определить допустимость параметра свойства **[value](field-value-property-dao.md)** для этого объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="3b32f-123">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object.</span></span> <span data-ttu-id="3b32f-124">Если для свойства **Required** задано значение **false**, поле может содержать значения **null** , а также значения, соответствующие условиям, заданным параметрами **пустые** и **ValidationRule** .</span><span class="sxs-lookup"><span data-stu-id="3b32f-124">If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="3b32f-125">Если вы можете задать это свойство для объекта **индекса** или объекта **field** , задайте для объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="3b32f-125">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object.</span></span> <span data-ttu-id="3b32f-126">Срок действия параметра свойства для объекта **field** проверяется до объекта **index** .</span><span class="sxs-lookup"><span data-stu-id="3b32f-126">The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="3b32f-127">Пример</span><span class="sxs-lookup"><span data-stu-id="3b32f-127">Example</span></span>

<span data-ttu-id="3b32f-128">В этом примере используется свойство **Required** , чтобы сообщить, какие поля в трех различных таблицах должны содержать данные, чтобы добавить новую запись.</span><span class="sxs-lookup"><span data-stu-id="3b32f-128">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added.</span></span> <span data-ttu-id="3b32f-129">Для выполнения этой процедуры требуется процедура Рекуиредаутпут.</span><span class="sxs-lookup"><span data-stu-id="3b32f-129">The RequiredOutput procedure is required for this procedure to run.</span></span>

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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

