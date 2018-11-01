---
title: Объекты объекта поля - доступ к данным (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4f8cf561c5e53de9da159c3aa5c8179a921deecf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867596"
---
# <a name="field-object-dao"></a><span data-ttu-id="5d074-102">Field Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d074-102">Field Object (DAO)</span></span>

<span data-ttu-id="5d074-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d074-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d074-104">Объект **поля** представляет столбец данных с типом данных и общий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="5d074-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d074-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="5d074-105">Remarks</span></span>

<span data-ttu-id="5d074-106">Коллекции **полей** **индекса**, **QueryDef**, **связь**и **TableDef** объектов содержат спецификаций для полей представляют эти объекты.</span><span class="sxs-lookup"><span data-stu-id="5d074-106">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent.</span></span> <span data-ttu-id="5d074-107">Коллекция **полей** объекта **набора записей** представляет объекты **поля** в строке данных или в записи.</span><span class="sxs-lookup"><span data-stu-id="5d074-107">The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record.</span></span> <span data-ttu-id="5d074-108">Используйте объекты **поля** в объекте **набора записей** для чтения и задайте значения для полей в текущей записи объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5d074-108">You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="5d074-109">В workspacee Microsoft Access управлять с помощью объекта **поля** , методы и свойства поля.</span><span class="sxs-lookup"><span data-stu-id="5d074-109">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties.</span></span> <span data-ttu-id="5d074-110">Например можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5d074-110">For example, you can:</span></span>

  - <span data-ttu-id="5d074-111">Свойство **OrdinalPosition** задает или возвращает порядок представления объекта **поля** в коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="5d074-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="5d074-112">Свойство **значение** поля в объекте **набора записей** или возвращает сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="5d074-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="5d074-113">Используйте **AppendChunk** и **GetChunk** методы и **свойства FieldSize** получить или задать значение в поле объекта OLE или Memo объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5d074-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="5d074-114">Использование свойств **типа**, **размер**и **атрибуты** для определения типа данных, которые могут храниться в поле.</span><span class="sxs-lookup"><span data-stu-id="5d074-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="5d074-115">Использование свойства **SourceField** и **Таблица** для определения исходного источника данных.</span><span class="sxs-lookup"><span data-stu-id="5d074-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="5d074-116">Свойство **ForeignName** задает или возвращает сведения о поле внешнего в объект **связи** .</span><span class="sxs-lookup"><span data-stu-id="5d074-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="5d074-117">Использование свойств **пустые строки**, **значение по умолчанию**, **необходимых**, **Проверка набора**, **значение**или **сообщение об ошибке** или возвращает условия проверки данных.</span><span class="sxs-lookup"><span data-stu-id="5d074-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="5d074-118">Свойство **DefaultValue** поля в объекте **TableDef** для установки значения по умолчанию для этого поля, при добавлении новых записей.</span><span class="sxs-lookup"><span data-stu-id="5d074-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="5d074-119">Чтобы создать новый объект **поля** в **индексе**, **TableDef**или объект **отношения** , используйте метод **CreateField** .</span><span class="sxs-lookup"><span data-stu-id="5d074-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="5d074-120">При получении доступа к объекту **поля** в составе объекта **набора записей** , данные из текущей записи отображается в свойство **Value** объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="5d074-120">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property.</span></span> <span data-ttu-id="5d074-121">Для работы с данными в объекте **набора записей** , не ссылки обычно коллекции **полей** напрямую. Вместо этого косвенно ссылки на свойство **Value** объекта **поля** в коллекции **полей** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="5d074-121">To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="5d074-122">Для ссылки на объект **поля** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="5d074-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="5d074-123">**Поля** (0)</span><span class="sxs-lookup"><span data-stu-id="5d074-123">**Fields**(0)</span></span>

- <span data-ttu-id="5d074-124">**Поля** («имя»)</span><span class="sxs-lookup"><span data-stu-id="5d074-124">**Fields**("name")</span></span>

- <span data-ttu-id="5d074-125">**Поля**\!\[имя\]</span><span class="sxs-lookup"><span data-stu-id="5d074-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="5d074-126">С помощью одной синтаксиса форм можно найти в свойство **Value** объекта **поля** , добавьте к коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="5d074-126">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection.</span></span> <span data-ttu-id="5d074-127">Контекст ссылку на поле определяет, будет ли вы ссылаетесь на объект **поля** или свойства **Value** объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="5d074-127">The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="5d074-128">Пример</span><span class="sxs-lookup"><span data-stu-id="5d074-128">Example</span></span>

<span data-ttu-id="5d074-129">В этом примере показано, какие свойства являются допустимыми для объекта **поля** в зависимости от того, где находится **поле** (для примера, коллекции **полей** **TableDef**, коллекции **полей** **QueryDef**и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5d074-129">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth).</span></span> <span data-ttu-id="5d074-130">Процедура FieldOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="5d074-130">The FieldOutput procedure is required for this procedure to run.</span></span>

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

В этом примере используется метод **CreateField** для создания трех **полей** для нового **TableDef**. Затем отображает свойства объектов **поля** , которые автоматически устанавливаются с помощью метода **CreateField** . <span data-ttu-id="5d074-133">(Во время создания **поля** пусты, значения свойств, не отображаются.)</span><span class="sxs-lookup"><span data-stu-id="5d074-133">(Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
