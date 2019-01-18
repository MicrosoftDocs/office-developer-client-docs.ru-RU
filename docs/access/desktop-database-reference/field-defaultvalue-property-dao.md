---
title: Свойство Field.DefaultValue (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 8a1c558b-c8f6-757d-c595-4e50b9b6ae3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197092(v=office.15)
ms:contentKeyID: 48546185
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fb4d3a4427db2b407b6a20507339fe83665c97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711737"
---
# <a name="fielddefaultvalue-property-dao"></a><span data-ttu-id="db177-102">Свойство Field.DefaultValue (DAO)</span><span class="sxs-lookup"><span data-stu-id="db177-102">Field.DefaultValue property (DAO)</span></span>


<span data-ttu-id="db177-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db177-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="db177-104">Задает или возвращает значение по умолчанию объекта **[поля](field-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="db177-104">Sets or returns the default value of a **[Field](field-object-dao.md)** object.</span></span> <span data-ttu-id="db177-105">Для объекта **поля** , еще не добавляется в конец коллекции **[полей](fields-collection-dao.md)** это свойство является чтение/запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="db177-105">For a **Field** object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="db177-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db177-106">Syntax</span></span>

<span data-ttu-id="db177-107">*выражение* . Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="db177-107">*expression* .DefaultValue</span></span>

<span data-ttu-id="db177-108">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="db177-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="db177-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="db177-109">Remarks</span></span>

<span data-ttu-id="db177-110">Параметр или возвращаемое значение имеет тип данных **String** , которое может содержать не более 255 знаков.</span><span class="sxs-lookup"><span data-stu-id="db177-110">The setting or return value is a **String** data type that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="db177-111">Она может быть текст или выражение.</span><span class="sxs-lookup"><span data-stu-id="db177-111">It can be either text or an expression.</span></span> <span data-ttu-id="db177-112">Если значение свойства — это выражение, не может содержать пользовательские функции, статистические функции ядра базы данных SQL Microsoft Access или ссылки на запросы, форм или других объектов **поля** .</span><span class="sxs-lookup"><span data-stu-id="db177-112">If the property setting is an expression, it can't contain user-defined functions, Microsoft Access database engine SQL aggregate functions, or references to queries, forms, or other **Field** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="db177-113">Также можно настроить свойство **DefaultValue** объекта **поля** на объект [TableDef](tabledef-object-dao.md) особое значение называется «(GenUniqueID)».</span><span class="sxs-lookup"><span data-stu-id="db177-113">You can also set the **DefaultValue** property of a **Field** object on a [TableDef](tabledef-object-dao.md) object to a special value called "GenUniqueID( )".</span></span> <span data-ttu-id="db177-114">В результате случайное число для назначения в этом поле каждый раз, когда добавляется или создать новую запись, тем самым обеспечивая каждой записи уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="db177-114">This causes a random number to be assigned to this field whenever a new record is added or created, thereby giving each record a unique identifier.</span></span> <span data-ttu-id="db177-115">[Тип](field-type-property-dao.md) поля должен быть **времени**.</span><span class="sxs-lookup"><span data-stu-id="db177-115">The field's [Type](field-type-property-dao.md) property must be **Long**.</span></span>


<span data-ttu-id="db177-116">Доступность **функции DefaultValue** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="db177-116">The availability of the **DefaultValue** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db177-117">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="db177-117">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="db177-118">Значение по умолчанию — это</span><span class="sxs-lookup"><span data-stu-id="db177-118">Then DefaultValue is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db177-119">Объект Index</span><span class="sxs-lookup"><span data-stu-id="db177-119">Index object</span></span></p></td>
<td><p><span data-ttu-id="db177-120">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db177-120">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db177-121">Объект QueryDef</span><span class="sxs-lookup"><span data-stu-id="db177-121">QueryDef object</span></span></p></td>
<td><p><span data-ttu-id="db177-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db177-122">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db177-123">Объект Recordset</span><span class="sxs-lookup"><span data-stu-id="db177-123">Recordset object</span></span></p></td>
<td><p><span data-ttu-id="db177-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="db177-124">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db177-125">Объект Relation</span><span class="sxs-lookup"><span data-stu-id="db177-125">Relation object</span></span></p></td>
<td><p><span data-ttu-id="db177-126">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db177-126">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db177-127">Объект TableDef</span><span class="sxs-lookup"><span data-stu-id="db177-127">TableDef object</span></span></p></td>
<td><p><span data-ttu-id="db177-128">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db177-128">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db177-129">При создании новой записи, значение свойства **DefaultValue** автоматически вводится как значение для поля.</span><span class="sxs-lookup"><span data-stu-id="db177-129">When a new record is created, the **DefaultValue** property setting is automatically entered as the value for the field.</span></span> <span data-ttu-id="db177-130">Значение поля можно изменить, задав его свойство **[Value](field-value-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="db177-130">You can change the field value by setting its **[Value](field-value-property-dao.md)** property.</span></span>

<span data-ttu-id="db177-131">Свойство **DefaultValue** не применяется к **счетчика** и **Длинные двоичные** поля.</span><span class="sxs-lookup"><span data-stu-id="db177-131">The **DefaultValue** property doesn't apply to **AutoNumber** and **Long Binary** fields.</span></span>

## <a name="example"></a><span data-ttu-id="db177-132">Пример</span><span class="sxs-lookup"><span data-stu-id="db177-132">Example</span></span>

<span data-ttu-id="db177-133">В этом примере используется свойство **DefaultValue** для оповещения пользователя Обычное значение поля во время запроса на ввода данных.</span><span class="sxs-lookup"><span data-stu-id="db177-133">This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input.</span></span> <span data-ttu-id="db177-134">Кроме того, он показывает, как новые записи будет состоять из с помощью **DefaultValue** при отсутствии другие входные данные.</span><span class="sxs-lookup"><span data-stu-id="db177-134">In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input.</span></span> <span data-ttu-id="db177-135">Функция DefaultPrompt является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="db177-135">The DefaultPrompt function is required for this procedure to run.</span></span>

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
     fldTemp As Field) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
