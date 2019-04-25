---
title: Объект Field — объекты DAO
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293044"
---
# <a name="field-object-dao"></a><span data-ttu-id="ef708-102">Объект Field (DAO)</span><span class="sxs-lookup"><span data-stu-id="ef708-102">Field Object (DAO)</span></span>

<span data-ttu-id="ef708-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef708-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef708-104">Объект **Field** представляет столбец данных с общим типом данных и общим набором свойств.</span><span class="sxs-lookup"><span data-stu-id="ef708-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef708-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef708-105">Remarks</span></span>

<span data-ttu-id="ef708-106">Коллекции **Fields** объектов **Index**, **QueryDef**, **Relation** и **TableDef** содержат спецификации для полей, представляемых этими объектами.</span><span class="sxs-lookup"><span data-stu-id="ef708-106">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent.</span></span> <span data-ttu-id="ef708-107">Коллекция **Fields** объекта **Recordset** представляет объекты **Field** в строке данных или в записи.</span><span class="sxs-lookup"><span data-stu-id="ef708-107">The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record.</span></span> <span data-ttu-id="ef708-108">Объекты **Field** в объекте **Recordset** используются для чтения и задания значений для полей в текущей записи объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef708-108">You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="ef708-109">В рабочей области Microsoft Access управление полем выполняется с помощью объекта **Field** и его методов и свойств.</span><span class="sxs-lookup"><span data-stu-id="ef708-109">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties.</span></span> <span data-ttu-id="ef708-110">Например, вы можете:</span><span class="sxs-lookup"><span data-stu-id="ef708-110">For example, you can:</span></span>

  - <span data-ttu-id="ef708-111">Использовать свойство **OrdinalPosition**, чтобы задать или вернуть порядок представления объекта **Field** в коллекции **Fields**.</span><span class="sxs-lookup"><span data-stu-id="ef708-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="ef708-112">Использовать свойство **Value** поля в объекте **Recordset**, чтобы задать или вернуть сохраняемые данные.</span><span class="sxs-lookup"><span data-stu-id="ef708-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="ef708-113">Использовать методы **AppendChunk** и **GetChunk**, а также свойство **FieldSize**, чтобы получить или задать значение в объекте OLE или поле Memo объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef708-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="ef708-114">Использовать свойства **Type**, **Size** и **Attributes**, чтобы определить тип данных, которые могут храниться в поле.</span><span class="sxs-lookup"><span data-stu-id="ef708-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="ef708-115">Использовать свойства **SourceField** и **SourceTable**, чтобы определить исходный источник данных.</span><span class="sxs-lookup"><span data-stu-id="ef708-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="ef708-116">Использовать свойство **ForeignName**, чтобы задать или получить сведения о внешнем поле в объекте **Relation**.</span><span class="sxs-lookup"><span data-stu-id="ef708-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="ef708-117">Использовать свойства **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** или **ValidationText**, чтобы задать или вернуть условия проверки.</span><span class="sxs-lookup"><span data-stu-id="ef708-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="ef708-118">Использовать свойство **DefaultValue** поля в объекте **TableDef**, чтобы задать значение по умолчанию для этого поля при добавлении новых записей.</span><span class="sxs-lookup"><span data-stu-id="ef708-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="ef708-119">Чтобы создать новый объект **Field** в объектах **Index**, **TableDef** или **Relation**, используйте метод **CreateField**.</span><span class="sxs-lookup"><span data-stu-id="ef708-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="ef708-120">При доступе к объекту **Field**, входящему в объект **Recordset**, данные из текущей записи отображаются в свойстве **Value** объекта **Field**.</span><span class="sxs-lookup"><span data-stu-id="ef708-120">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property.</span></span> <span data-ttu-id="ef708-121">Чтобы управлять данными в объекте **Recordset**, обычно не используется прямая ссылка на коллекцию **Fields**; вместо этого используется косвенная ссылка на свойство **Value** объекта **Field** в коллекции **Fields** объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="ef708-121">To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="ef708-122">Чтобы сослаться на объект **Field** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="ef708-122">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="ef708-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="ef708-123">**Fields**(0)</span></span>

- <span data-ttu-id="ef708-124">**Fields**("name")</span><span class="sxs-lookup"><span data-stu-id="ef708-124">**Fields**("name")</span></span>

- <span data-ttu-id="ef708-125">**Fields**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="ef708-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="ef708-126">С помощью этих синтаксических форм можно также ссылаться на свойство **Value** созданного объекта **Field**, добавляемого в коллекцию **Fields**.</span><span class="sxs-lookup"><span data-stu-id="ef708-126">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection.</span></span> <span data-ttu-id="ef708-127">Контекст ссылки на поле определяет, ссылаетесь ли вы на объект **Field** или свойство **Value** объекта **Field**.</span><span class="sxs-lookup"><span data-stu-id="ef708-127">The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="ef708-128">Пример</span><span class="sxs-lookup"><span data-stu-id="ef708-128">Example</span></span>

<span data-ttu-id="ef708-129">В этом примере показано, какие свойства допустимы для объекта **Field** в зависимости от расположения объекта **Field** (например, в коллекции **Fields** объекта **TableDef**, коллекции **Fields** объекта **QueryDef** и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ef708-129">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth).</span></span> <span data-ttu-id="ef708-130">Процедура FieldOutput является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="ef708-130">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

В этом примере используется метод **CreateField** для создания трех объектов **Field** для нового объекта **TableDef**. После этого отображаются свойства этих объектов **Field**, автоматически устанавливаемые методом **CreateField**. <span data-ttu-id="ef708-133">(Свойства, у которых отсутствуют значения во время создания объекта **Field**, не отображаются.)</span><span class="sxs-lookup"><span data-stu-id="ef708-133">(Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
