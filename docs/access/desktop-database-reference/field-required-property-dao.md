---
title: Свойство Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25ba678f759fefa460dd505cded6e05b3e96fdf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928357"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="28d29-102">Свойство Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="28d29-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="28d29-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28d29-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28d29-104">Задает или возвращает значение, которое указывает, требуется ли объект **[поля](field-object-dao.md)** ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="28d29-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28d29-105">Syntax</span></span>

<span data-ttu-id="28d29-106">*выражение* . Обязательно</span><span class="sxs-lookup"><span data-stu-id="28d29-106">*expression* .Required</span></span>

<span data-ttu-id="28d29-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="28d29-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d29-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="28d29-108">Remarks</span></span>

<span data-ttu-id="28d29-109">Для **поля** еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="28d29-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="28d29-110">Доступность свойства **необходимые** зависит от объекта, который содержит коллекцию [полей](fields-collection-dao.md) , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="28d29-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28d29-111">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="28d29-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="28d29-112">Затем необходимо — это</span><span class="sxs-lookup"><span data-stu-id="28d29-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28d29-113">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="28d29-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28d29-114">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="28d29-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d29-115">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="28d29-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28d29-116">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28d29-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d29-117">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="28d29-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28d29-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28d29-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="28d29-119"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="28d29-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28d29-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="28d29-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="28d29-121">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="28d29-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="28d29-122">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="28d29-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="28d29-123">Свойства **необходимые** вместе со свойством **[пустые строки](field-allowzerolength-property-dao.md)**, **[Проверка набора](field-validateonset-property-dao.md)** или **[значение](field-validationrule-property-dao.md)** можно использовать для определения действительности значение свойства **[значение](field-value-property-dao.md)** для этого объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="28d29-123">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object.</span></span> <span data-ttu-id="28d29-124">Если **требуется** свойство имеет значение **False**, поле может содержать значения **null** , а также значения, которые соответствуют условиям, указанным в параметрах свойство **пустые строки** и **значение** .</span><span class="sxs-lookup"><span data-stu-id="28d29-124">If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="28d29-125">При установке этого свойства для объекта <STRONG>индекса</STRONG> или объекта <STRONG>поля</STRONG> задайте его для объекта <STRONG>поля</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="28d29-125">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object.</span></span> <span data-ttu-id="28d29-126">Перед, объект <STRONG>индекса</STRONG> проверять правильность настройки свойства для объекта <STRONG>поля</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="28d29-126">The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="28d29-127">Пример</span><span class="sxs-lookup"><span data-stu-id="28d29-127">Example</span></span>

<span data-ttu-id="28d29-128">В этом примере используется свойство **требуется** отчет о котором поля в три различных таблицы должен содержать данные в порядке для новой записи для добавления.</span><span class="sxs-lookup"><span data-stu-id="28d29-128">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added.</span></span> <span data-ttu-id="28d29-129">Процедура RequiredOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="28d29-129">The RequiredOutput procedure is required for this procedure to run.</span></span>

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

