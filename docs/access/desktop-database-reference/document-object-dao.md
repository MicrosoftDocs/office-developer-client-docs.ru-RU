---
title: Объект Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4dbd7de05a3bb2402d436e4bbac59f1ca4687317
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026332"
---
# <a name="document-object-dao"></a><span data-ttu-id="1174f-102">Объект Document (DAO)</span><span class="sxs-lookup"><span data-stu-id="1174f-102">Document object (DAO)</span></span>

<span data-ttu-id="1174f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1174f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1174f-104">Объект **Document** содержит сведения о один экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="1174f-104">A **Document** object includes information about one instance of an object.</span></span> <span data-ttu-id="1174f-105">Объект может быть базы данных, сохраненные в таблице, запрос или связь (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="1174f-105">The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="1174f-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="1174f-106">Remarks</span></span>

<span data-ttu-id="1174f-107">Каждый объект- **контейнер** имеет **документы** коллекцию, содержащую объекты **документов** , которые описывают экземпляры встроенные объекты типа, указанного в качестве **контейнера**.</span><span class="sxs-lookup"><span data-stu-id="1174f-107">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="1174f-108">В следующей таблице перечислены тип объекта, который описывает каждого **документа** , имя его объекта- **контейнера** , а какая информация **документ** содержит.</span><span class="sxs-lookup"><span data-stu-id="1174f-108">The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1174f-109">Документ</span><span class="sxs-lookup"><span data-stu-id="1174f-109">Document</span></span></p></th>
<th><p><span data-ttu-id="1174f-110">Container</span><span class="sxs-lookup"><span data-stu-id="1174f-110">Container</span></span></p></th>
<th><p><span data-ttu-id="1174f-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="1174f-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1174f-112">База данных</span><span class="sxs-lookup"><span data-stu-id="1174f-112">Database</span></span></p></td>
<td><p><span data-ttu-id="1174f-113">Databases</span><span class="sxs-lookup"><span data-stu-id="1174f-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="1174f-114">Сохраненные базы данных</span><span class="sxs-lookup"><span data-stu-id="1174f-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1174f-115">Таблица или запрос</span><span class="sxs-lookup"><span data-stu-id="1174f-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="1174f-116">Таблицы</span><span class="sxs-lookup"><span data-stu-id="1174f-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="1174f-117">Сохранить таблицы или запроса</span><span class="sxs-lookup"><span data-stu-id="1174f-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1174f-118">Связь</span><span class="sxs-lookup"><span data-stu-id="1174f-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="1174f-119">Relations</span><span class="sxs-lookup"><span data-stu-id="1174f-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="1174f-120">Сохраненные отношения</span><span class="sxs-lookup"><span data-stu-id="1174f-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1174f-121">Не следует путать объекты **контейнеров** , перечисленных в предыдущей таблице с семействами с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="1174f-121">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="1174f-122">Баз данных **контейнер** объекта ссылается на все объекты сохраненного базы данных, но семейства **баз данных** относится только к объекты базы данных, которые открыты в конкретной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1174f-122">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="1174f-123">Объект **Document** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1174f-123">With a **Document** object, you can:</span></span>

- <span data-ttu-id="1174f-124">Используйте свойство **Name** возвращает имя, которое пользователь или ядро базы данных Microsoft Access присваивает объекту при его создании.</span><span class="sxs-lookup"><span data-stu-id="1174f-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

- <span data-ttu-id="1174f-125">Свойство **контейнера** возвращает имя объекта **контейнера** , который содержит объект **Document** .</span><span class="sxs-lookup"><span data-stu-id="1174f-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

- <span data-ttu-id="1174f-126">Используйте свойство **владельца** или возвращает владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="1174f-126">Use the **Owner** property to set or return the owner of the object.</span></span> <span data-ttu-id="1174f-127">Для установки свойства **Owner** , необходимо иметь разрешения на запись для объекта **Document** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="1174f-127">To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="1174f-128">Использование свойств **имя пользователя** или **разрешения** или возвращает разрешения на доступ к пользователю или группе для объекта.</span><span class="sxs-lookup"><span data-stu-id="1174f-128">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object.</span></span> <span data-ttu-id="1174f-129">Чтобы задать эти свойства, необходимо иметь разрешения на запись для объекта **Document** , а свойство **UserName** необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="1174f-129">To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="1174f-130">Использование свойства **DateCreated** и **LastUpdated** возвращает дату и время создания и последнего изменения объекта **Document** .</span><span class="sxs-lookup"><span data-stu-id="1174f-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="1174f-131">Поскольку объект **Document** соответствует существующий объект, не могут создавать новые объекты **документа** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="1174f-131">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones.</span></span> <span data-ttu-id="1174f-132">Для ссылки на объект **Document** в семействе сайтов, с его порядковый номер или **его свойства Name** , используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="1174f-132">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="1174f-133">**Документы** (0)</span><span class="sxs-lookup"><span data-stu-id="1174f-133">**Documents**(0)</span></span>

- <span data-ttu-id="1174f-134">**Документы** («*имя*»)</span><span class="sxs-lookup"><span data-stu-id="1174f-134">**Documents**("*name*")</span></span>

- <span data-ttu-id="1174f-135">**Документы**\!\[*имя*\]</span><span class="sxs-lookup"><span data-stu-id="1174f-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="1174f-136">Пример</span><span class="sxs-lookup"><span data-stu-id="1174f-136">Example</span></span>

<span data-ttu-id="1174f-137">В этом примере создается перечисление коллекции **документов** контейнер таблиц и затем создается перечисление коллекции **свойств** первый объект **документа** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1174f-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="1174f-138">В этом примере используются свойства **владельца** и **SystemDB** для отображения владельцев различных объектов **документа** .</span><span class="sxs-lookup"><span data-stu-id="1174f-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

