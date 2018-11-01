---
title: Properties Collection (DAO)
TOCTitle: Properties Collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f30ccd48ee5e4f4815be4d7e1ec6d94f237bc16
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874288"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="9ca45-102">Properties Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ca45-102">Properties Collection (DAO)</span></span>


<span data-ttu-id="9ca45-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ca45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ca45-104">Коллекция **свойств** содержит все объекты **[Свойства](property-object-dao.md)** для указанного экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca45-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca45-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ca45-105">Remarks</span></span>

<span data-ttu-id="9ca45-106">Каждый объект DAO, за исключением **подключения** и объектов **ошибок** содержит коллекцию **свойств** , которая имеет определенных встроенных **свойств** объектов.</span><span class="sxs-lookup"><span data-stu-id="9ca45-106">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects.</span></span> <span data-ttu-id="9ca45-107">Эти объекты **свойство** (которые часто просто называются свойства) однозначно Создание характеристик этого экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca45-107">These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="9ca45-108">Кроме встроенных свойств можно также создать и добавить свои собственные пользовательские свойства.</span><span class="sxs-lookup"><span data-stu-id="9ca45-108">In addition to the built-in properties, you can also create and add your own user-defined properties.</span></span> <span data-ttu-id="9ca45-109">Чтобы добавить пользовательские свойства существующего экземпляра объекта, сначала определите его характеристики с помощью метода **CreateProperty** , а затем добавить его в коллекцию с помощью метода **Append** .</span><span class="sxs-lookup"><span data-stu-id="9ca45-109">To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method.</span></span> <span data-ttu-id="9ca45-110">Создание ссылок на объект пользовательские **Свойства** , который еще не была добавлена к коллекции **свойств** вызовет ошибку, как и добавление объект пользовательских **свойств** в коллекцию **свойств** , содержащую \*\* Свойство\*\* объект с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="9ca45-110">Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="9ca45-111">Можно использовать метод **Delete** для удаления пользовательских свойств из коллекции **свойств** , но вы не можете удалить встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="9ca45-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9ca45-112">Объект пользовательских <STRONG>свойств</STRONG> сопоставляется только с определенный экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca45-112">A user-defined <STRONG>Property</STRONG> object is associated only with the specific instance of an object.</span></span> <span data-ttu-id="9ca45-113">Свойство не определено для всех экземпляров объектов выбранного типа.</span><span class="sxs-lookup"><span data-stu-id="9ca45-113">The property isn't defined for all instances of objects of the selected type.</span></span></P>



<span data-ttu-id="9ca45-114">Для ссылки на объект встроенных **свойств** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="9ca45-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9ca45-115">объект. **Свойства** (0)</span><span class="sxs-lookup"><span data-stu-id="9ca45-115">object.**Properties**(0)</span></span>

<span data-ttu-id="9ca45-116">объект. **Свойства** («имя»)</span><span class="sxs-lookup"><span data-stu-id="9ca45-116">object.**Properties**("name")</span></span>

<span data-ttu-id="9ca45-117">объект. **Свойства** \! \[имя\]</span><span class="sxs-lookup"><span data-stu-id="9ca45-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="9ca45-118">Для встроенных свойств можно также используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="9ca45-118">For a built-in property, you can also use this syntax:</span></span>

<span data-ttu-id="9ca45-119">Object.Name</span><span class="sxs-lookup"><span data-stu-id="9ca45-119">object.name</span></span>


> [!NOTE]
> <P><span data-ttu-id="9ca45-120">Пользовательские свойства необходимо использовать полный объект. <STRONG>Свойства</STRONG> синтаксис («имя»).</span><span class="sxs-lookup"><span data-stu-id="9ca45-120">For a user-defined property, you must use the full object.<STRONG>Properties</STRONG>("name") syntax.</span></span></P>



<span data-ttu-id="9ca45-121">С помощью одной синтаксиса форм можно найти в свойство **Value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="9ca45-121">With the same syntax forms, you can also refer to the **Value** property of a **Property** object.</span></span> <span data-ttu-id="9ca45-122">Контекст ссылки определяет, будет ли вы ссылаетесь на объект **свойств** , самого или свойство **Value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="9ca45-122">The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="9ca45-123">Пример</span><span class="sxs-lookup"><span data-stu-id="9ca45-123">Example</span></span>

<span data-ttu-id="9ca45-124">В этом примере создается пользовательское свойство в текущей базе данных, задает его **Тип** и **значение** свойства и добавляет его в коллекцию **свойств** базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ca45-124">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database.</span></span> <span data-ttu-id="9ca45-125">Затем в примере перечисляются все свойства в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9ca45-125">Then the example enumerates all properties in the database.</span></span>

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

<span data-ttu-id="9ca45-126">В этом примере предпринимается попытка задать значение свойства пользовательских.</span><span class="sxs-lookup"><span data-stu-id="9ca45-126">This example tries to set the value of a user-defined property.</span></span> <span data-ttu-id="9ca45-127">Если свойство не существует, метод **CreateProperty** используется для создания и установите значение нового свойства.</span><span class="sxs-lookup"><span data-stu-id="9ca45-127">If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property.</span></span> <span data-ttu-id="9ca45-128">Процедура SetProperty является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="9ca45-128">The SetProperty procedure is required for this procedure to run.</span></span>

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
