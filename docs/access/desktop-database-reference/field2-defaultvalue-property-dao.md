---
title: Свойство field2. DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845a2e0c7ffa5d54d73c4fcec1a6c785468d734e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292834"
---
# <a name="field2defaultvalue-property-dao"></a><span data-ttu-id="2f564-102">Свойство field2. DefaultValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f564-102">Field2.DefaultValue property (DAO)</span></span>

<span data-ttu-id="2f564-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f564-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f564-104">Задает или возвращает значение, заданное по умолчанию для объекта **field2** .</span><span class="sxs-lookup"><span data-stu-id="2f564-104">Sets or returns the default value of a **Field2** object.</span></span> <span data-ttu-id="2f564-105">Для объекта **field2** , еще не добавленного в коллекцию **[Fields](fields-collection-dao.md)** , это свойство доступно для чтения и записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2f564-105">For a **Field2** object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f564-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f564-106">Syntax</span></span>

<span data-ttu-id="2f564-107">*Expression* . Значение</span><span class="sxs-lookup"><span data-stu-id="2f564-107">*expression* .DefaultValue</span></span>

<span data-ttu-id="2f564-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="2f564-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f564-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f564-109">Remarks</span></span>

<span data-ttu-id="2f564-110">Параметр или возвращаемое значение — это **строковый** тип данных, который может содержать не более 255 символов.</span><span class="sxs-lookup"><span data-stu-id="2f564-110">The setting or return value is a **String** data type that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="2f564-111">Это может быть либо Text, либо Expression.</span><span class="sxs-lookup"><span data-stu-id="2f564-111">It can be either text or an expression.</span></span> <span data-ttu-id="2f564-112">Если параметр свойства является выражением, он не может содержать пользовательские функции, статистические функции SQL ядра СУБД Microsoft Access или ссылки на запросы, формы или другие объекты **field2** .</span><span class="sxs-lookup"><span data-stu-id="2f564-112">If the property setting is an expression, it can't contain user-defined functions, Microsoft Access database engine SQL aggregate functions, or references to queries, forms, or other **Field2** objects.</span></span>

> [!NOTE]
> <span data-ttu-id="2f564-113">Кроме того, можно задать для свойства **DefaultValue** объекта **field2** в объекте **tabledef** специальное значение с именем "женуникуеид ()".</span><span class="sxs-lookup"><span data-stu-id="2f564-113">You can also set the **DefaultValue** property of a **Field2** object on a **TableDef** object to a special value called "GenUniqueID( )".</span></span> <span data-ttu-id="2f564-114">Это приводит к тому, что это поле назначается случайному числу при добавлении или создании новой записи, таким образом выдавая каждой записи уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2f564-114">This causes a random number to be assigned to this field whenever a new record is added or created, thereby giving each record a unique identifier.</span></span> <span data-ttu-id="2f564-115">Свойство **типа** поля должно быть длинным \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="2f564-115">The field's **Type** property must be **Long**.</span></span>

<span data-ttu-id="2f564-116">Доступность свойства **DefaultValue** зависит от объекта, содержащего коллекцию Fields, как \*\*\*\* показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2f564-116">The availability of the **DefaultValue** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f564-117">Если коллекция Fields принадлежит к элементу</span><span class="sxs-lookup"><span data-stu-id="2f564-117">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="2f564-118">Значение DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2f564-118">Then DefaultValue is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f564-119">Объект Index</span><span class="sxs-lookup"><span data-stu-id="2f564-119">Index object</span></span></p></td>
<td><p><span data-ttu-id="2f564-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f564-120">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f564-121">Объект QueryDef</span><span class="sxs-lookup"><span data-stu-id="2f564-121">QueryDef object</span></span></p></td>
<td><p><span data-ttu-id="2f564-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f564-122">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f564-123">Объект Recordset</span><span class="sxs-lookup"><span data-stu-id="2f564-123">Recordset object</span></span></p></td>
<td><p><span data-ttu-id="2f564-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="2f564-124">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f564-125">Объект Relation</span><span class="sxs-lookup"><span data-stu-id="2f564-125">Relation object</span></span></p></td>
<td><p><span data-ttu-id="2f564-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f564-126">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f564-127">Объект TableDef</span><span class="sxs-lookup"><span data-stu-id="2f564-127">TableDef object</span></span></p></td>
<td><p><span data-ttu-id="2f564-128">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2f564-128">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f564-129">При создании новой записи параметр свойства **DefaultValue** автоматически вводится в качестве значения для поля.</span><span class="sxs-lookup"><span data-stu-id="2f564-129">When a new record is created, the **DefaultValue** property setting is automatically entered as the value for the field.</span></span> <span data-ttu-id="2f564-130">Значение поля можно изменить, задав его свойство **value** .</span><span class="sxs-lookup"><span data-stu-id="2f564-130">You can change the field value by setting its **Value** property.</span></span>

<span data-ttu-id="2f564-131">Свойство **DefaultValue** не применяется к полям **счетчика** и **длинным двоичным** полям.</span><span class="sxs-lookup"><span data-stu-id="2f564-131">The **DefaultValue** property doesn't apply to **AutoNumber** and **Long Binary** fields.</span></span>

## <a name="example"></a><span data-ttu-id="2f564-132">Пример</span><span class="sxs-lookup"><span data-stu-id="2f564-132">Example</span></span>

<span data-ttu-id="2f564-133">В этом примере используется свойство **DefaultValue** для оповещения пользователя о обычном значении поля при запросе ввода.</span><span class="sxs-lookup"><span data-stu-id="2f564-133">This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input.</span></span> <span data-ttu-id="2f564-134">Кроме того, в нем показано, как новые записи будут заполнены с использованием **DefaultValue** при отсутствии других входных данных.</span><span class="sxs-lookup"><span data-stu-id="2f564-134">In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input.</span></span> <span data-ttu-id="2f564-135">Для выполнения этой процедуры требуется функция Дефаултпромпт.</span><span class="sxs-lookup"><span data-stu-id="2f564-135">The DefaultPrompt function is required for this procedure to run.</span></span>

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
