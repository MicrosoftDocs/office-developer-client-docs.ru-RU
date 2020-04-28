---
title: Коллекция Properties (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 515d28f0d7d99359c36df79cf3b8769d8f71e06d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301283"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="9a5b2-102">Коллекция Properties (DAO)</span><span class="sxs-lookup"><span data-stu-id="9a5b2-102">Properties collection (DAO)</span></span>

<span data-ttu-id="9a5b2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a5b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a5b2-104">Коллекция **Properties** содержит все объекты **[Property](property-object-dao.md)** для определенного экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a5b2-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a5b2-105">Remarks</span></span>

<span data-ttu-id="9a5b2-106">Каждый объект DAO, за исключением объектов **Connection** и **Error** , содержит коллекцию **Properties** , у которой есть некоторые встроенные объекты **Property** .</span><span class="sxs-lookup"><span data-stu-id="9a5b2-106">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects.</span></span> <span data-ttu-id="9a5b2-107">Эти объекты **свойств** (часто называемые свойствами) однозначно характеризуют экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-107">These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="9a5b2-108">В дополнение к встроенным свойствам можно также создавать и добавлять собственные пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-108">In addition to the built-in properties, you can also create and add your own user-defined properties.</span></span> <span data-ttu-id="9a5b2-109">Чтобы добавить пользовательское свойство в существующий экземпляр объекта, сначала определите его характеристики с помощью метода **CreateProperty** , а затем добавьте его в коллекцию с помощью метода **append** .</span><span class="sxs-lookup"><span data-stu-id="9a5b2-109">To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method.</span></span> <span data-ttu-id="9a5b2-110">Обращение к объекту пользовательского **Свойства** , еще не добавленному в коллекцию **свойств** , приведет к ошибке, так как добавляет пользовательский объект **Свойства** в коллекцию **свойств** , содержащую объект **Property** с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-110">Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="9a5b2-111">С помощью метода **Delete** можно удалять пользовательские свойства из коллекции **свойств** , но нельзя удалять встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="9a5b2-112">Объект определяемого пользователем **Свойства** связан только с определенным экземпляром объекта.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-112">A user-defined **Property** object is associated only with the specific instance of an object.</span></span> <span data-ttu-id="9a5b2-113">Свойство не определено для всех экземпляров объектов выбранного типа.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-113">The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="9a5b2-114">Чтобы сослаться на встроенный объект **Property** в коллекции по его порядковому номеру или по его свойству **Name** , используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="9a5b2-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="9a5b2-115">объектам. **Свойства**(0)</span><span class="sxs-lookup"><span data-stu-id="9a5b2-115">object.**Properties**(0)</span></span>

- <span data-ttu-id="9a5b2-116">объектам. **Свойства**("имя")</span><span class="sxs-lookup"><span data-stu-id="9a5b2-116">object.**Properties**("name")</span></span>

- <span data-ttu-id="9a5b2-117">объектам. Имя **Свойства**\!\[\]</span><span class="sxs-lookup"><span data-stu-id="9a5b2-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="9a5b2-118">Для встроенного свойства также можно использовать следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="9a5b2-118">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="9a5b2-119">object.name</span><span class="sxs-lookup"><span data-stu-id="9a5b2-119">object.name</span></span>

> [!NOTE]
> <span data-ttu-id="9a5b2-120">Для свойства, определяемого пользователем, необходимо использовать весь объект. Синтаксис **свойств**("имя").</span><span class="sxs-lookup"><span data-stu-id="9a5b2-120">For a user-defined property, you must use the full object.**Properties**("name") syntax.</span></span>

<span data-ttu-id="9a5b2-121">Используя те же формы синтаксиса, вы также можете ссылаться на свойство **value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="9a5b2-121">With the same syntax forms, you can also refer to the **Value** property of a **Property** object.</span></span> <span data-ttu-id="9a5b2-122">Контекст ссылки определяет, будет ли ссылка на сам объект **Property** или свойство **value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="9a5b2-122">The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="9a5b2-123">Пример</span><span class="sxs-lookup"><span data-stu-id="9a5b2-123">Example</span></span>

<span data-ttu-id="9a5b2-124">В этом примере создается пользовательское свойство для текущей базы данных, задаются его свойства **Type** и **value** , а затем она добавляется в коллекцию **свойств** базы данных.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-124">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database.</span></span> <span data-ttu-id="9a5b2-125">Затем в примере перечисляются все свойства в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-125">Then the example enumerates all properties in the database.</span></span>

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="9a5b2-126">В этом примере предпринимается попытка задать значение определяемого пользователем свойства.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-126">This example tries to set the value of a user-defined property.</span></span> <span data-ttu-id="9a5b2-127">Если свойство не существует, оно использует метод **CreateProperty** , чтобы создать и задать значение нового свойства.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-127">If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property.</span></span> <span data-ttu-id="9a5b2-128">Для выполнения этой процедуры требуется процедура SetProperty.</span><span class="sxs-lookup"><span data-stu-id="9a5b2-128">The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
