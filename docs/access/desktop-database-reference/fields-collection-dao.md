---
title: Коллекция Fields (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: d87d1535afeaf0740627a7af3852b1929a0e6d50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292533"
---
# <a name="fields-collection-dao"></a><span data-ttu-id="9e488-102">Коллекция Fields (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e488-102">Fields Collection (DAO)</span></span>


<span data-ttu-id="9e488-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e488-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e488-104">Коллекция **Fields** содержит все сохраненные объекты **Field** объекта **Index**, **QueryDef**, **Recordset**, **Relation** или **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="9e488-104">A **Fields** collection contains all stored **Field** objects of an **Index**, **QueryDef**, **Recordset**, **Relation**, or **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e488-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e488-105">Remarks</span></span>

<span data-ttu-id="9e488-106">Коллекции **Fields** объектов **Index**, **QueryDef**, **Relation** и **TableDef** содержат спецификации для полей, представляемых этими объектами.</span><span class="sxs-lookup"><span data-stu-id="9e488-106">The **Fields** collections of the **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent.</span></span> <span data-ttu-id="9e488-107">Коллекция **Fields** объекта **Recordset** представляет объекты **Field** в строке данных или в записи.</span><span class="sxs-lookup"><span data-stu-id="9e488-107">The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record.</span></span> <span data-ttu-id="9e488-108">Объекты **Field** в объекте **Recordset** используются для чтения и задания значений для полей в текущей записи объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9e488-108">You use the **Field** objects in a **Recordset** object to read and to set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="9e488-109">Чтобы сослаться на объект **Field** в коллекции по его порядковому номеру или по его свойству**Name**, используйте любую из указанных ниже синтаксических форм.</span><span class="sxs-lookup"><span data-stu-id="9e488-109">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9e488-110">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="9e488-110">**Fields**(0)</span></span>

<span data-ttu-id="9e488-111">**Fields**("name")</span><span class="sxs-lookup"><span data-stu-id="9e488-111">**Fields**("name")</span></span>

<span data-ttu-id="9e488-112">**Fields**\!\[name\]</span><span class="sxs-lookup"><span data-stu-id="9e488-112">**Fields**\!\[name\]</span></span>

<span data-ttu-id="9e488-113">С помощью этих синтаксических форм можно также ссылаться на свойство **Value** созданного объекта **Field**, добавляемого в коллекцию **Fields**.</span><span class="sxs-lookup"><span data-stu-id="9e488-113">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection.</span></span> <span data-ttu-id="9e488-114">Контекст ссылки на поле определяет, ссылаетесь ли вы на объект **Field** или свойство **Value** объекта **Field**.</span><span class="sxs-lookup"><span data-stu-id="9e488-114">The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="9e488-115">Пример</span><span class="sxs-lookup"><span data-stu-id="9e488-115">Example</span></span>

<span data-ttu-id="9e488-116">В этом примере показано, какие свойства допустимы для объекта **Field** в зависимости от расположения объекта **Field** (например, в коллекции **Fields** объекта **TableDef**, коллекции **Fields** объекта **QueryDef** и т. д.).</span><span class="sxs-lookup"><span data-stu-id="9e488-116">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth).</span></span> <span data-ttu-id="9e488-117">Процедура FieldOutput является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9e488-117">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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

В этом примере используется метод **CreateField** для создания трех объектов **Field** для нового объекта **TableDef**. После этого отображаются свойства этих объектов **Field**, автоматически устанавливаемые методом **CreateField**. <span data-ttu-id="9e488-120">(Свойства, у которых отсутствуют значения во время создания объекта **Field**, не отображаются.)</span><span class="sxs-lookup"><span data-stu-id="9e488-120">(Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
