---
title: Объект Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f82ace31a991a6700417d4c0d66bf775fcb7b26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293779"
---
# <a name="document-object-dao"></a><span data-ttu-id="4851f-102">Объект Document (DAO)</span><span class="sxs-lookup"><span data-stu-id="4851f-102">Document object (DAO)</span></span>

<span data-ttu-id="4851f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4851f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4851f-104">Объект **Document** включает сведения об одном экземпляре объекта.</span><span class="sxs-lookup"><span data-stu-id="4851f-104">A **Document** object includes information about one instance of an object.</span></span> <span data-ttu-id="4851f-105">Объект может быть базой данных, сохраненной таблицей, запросом или отношением (только для баз данных я могу использовать яд баз данных Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4851f-105">The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="4851f-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="4851f-106">Remarks</span></span>

<span data-ttu-id="4851f-107">Каждый **объект** Container имеет коллекцию **Documents,** содержащую объекты **Document,** которые описывают экземпляры встроенных объектов типа, указанного **контейнером.**</span><span class="sxs-lookup"><span data-stu-id="4851f-107">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="4851f-108">В следующей таблице перечислены  тип объекта, описываемого в документе, имя его **объекта-контейнера** и тип сведений, которые содержит **документ.**</span><span class="sxs-lookup"><span data-stu-id="4851f-108">The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4851f-109">Document</span><span class="sxs-lookup"><span data-stu-id="4851f-109">Document</span></span></p></th>
<th><p><span data-ttu-id="4851f-110">Container</span><span class="sxs-lookup"><span data-stu-id="4851f-110">Container</span></span></p></th>
<th><p><span data-ttu-id="4851f-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="4851f-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4851f-112">Database</span><span class="sxs-lookup"><span data-stu-id="4851f-112">Database</span></span></p></td>
<td><p><span data-ttu-id="4851f-113">Базы данных</span><span class="sxs-lookup"><span data-stu-id="4851f-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="4851f-114">Сохраненная база данных</span><span class="sxs-lookup"><span data-stu-id="4851f-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4851f-115">Таблица или запрос</span><span class="sxs-lookup"><span data-stu-id="4851f-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="4851f-116">Таблицы</span><span class="sxs-lookup"><span data-stu-id="4851f-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="4851f-117">Сохраненная таблица или запрос</span><span class="sxs-lookup"><span data-stu-id="4851f-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4851f-118">Связь</span><span class="sxs-lookup"><span data-stu-id="4851f-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="4851f-119">Relations</span><span class="sxs-lookup"><span data-stu-id="4851f-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="4851f-120">Сохраненная связь</span><span class="sxs-lookup"><span data-stu-id="4851f-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4851f-121">Не путайте **объекты-контейнеры,** перечисленные в предыдущей таблице, с коллекциями с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="4851f-121">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="4851f-122">Объект **контейнера databases** ссылается на все сохраненные объекты базы данных, но коллекция **Databases** ссылается только на объекты баз данных, открытые в определенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4851f-122">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="4851f-123">С помощью **объекта Document** вы можете:</span><span class="sxs-lookup"><span data-stu-id="4851f-123">With a **Document** object, you can:</span></span>

- <span data-ttu-id="4851f-124">Используйте свойство **Name,** чтобы вернуть имя, которое пользователь или яд баз данных Microsoft Access предоставил объекту при его создания.</span><span class="sxs-lookup"><span data-stu-id="4851f-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

- <span data-ttu-id="4851f-125">Используйте свойство **Container,** чтобы вернуть имя объекта **Container,** который содержит **объект Document.**</span><span class="sxs-lookup"><span data-stu-id="4851f-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

- <span data-ttu-id="4851f-126">Используйте свойство **Owner,** чтобы установить или вернуть владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="4851f-126">Use the **Owner** property to set or return the owner of the object.</span></span> <span data-ttu-id="4851f-127">Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание для объекта **Document** и установить для свойства имя существующего объекта **User** или **Group.**</span><span class="sxs-lookup"><span data-stu-id="4851f-127">To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="4851f-128">Используйте свойства **UserName** или **Permissions,** чтобы установить или вернуть разрешения доступа пользователя или группы для объекта.</span><span class="sxs-lookup"><span data-stu-id="4851f-128">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object.</span></span> <span data-ttu-id="4851f-129">Чтобы установить эти свойства, необходимо иметь разрешение на написание для объекта **Document,** а для свойства **UserName** необходимо установить имя существующего объекта **User** или **Group.**</span><span class="sxs-lookup"><span data-stu-id="4851f-129">To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="4851f-130">Используйте свойства **DateCreated** и **LastUpdated** для возврата даты и времени создания и последнего изменения объекта **Document.**</span><span class="sxs-lookup"><span data-stu-id="4851f-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="4851f-131">Так как **объект Document** соответствует существующему объекту, нельзя создавать новые объекты **Document** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="4851f-131">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones.</span></span> <span data-ttu-id="4851f-132">Чтобы сослаться **на объект Document** в коллекции по порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис форм:</span><span class="sxs-lookup"><span data-stu-id="4851f-132">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="4851f-133">**Документы**(0)</span><span class="sxs-lookup"><span data-stu-id="4851f-133">**Documents**(0)</span></span>

- <span data-ttu-id="4851f-134">**Документы**("*имя")*</span><span class="sxs-lookup"><span data-stu-id="4851f-134">**Documents**("*name*")</span></span>

- <span data-ttu-id="4851f-135"> \! Документы \[ *name*\]</span><span class="sxs-lookup"><span data-stu-id="4851f-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="4851f-136">Пример</span><span class="sxs-lookup"><span data-stu-id="4851f-136">Example</span></span>

<span data-ttu-id="4851f-137">В этом примере включается enumerates the **Documents** collection of the Tables container, а затем — коллекция **Properties** первого объекта **Document** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="4851f-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

<span data-ttu-id="4851f-138">В этом примере **свойства Owner** и **SystemDB** используются для показа владельцев различных объектов **Document.**</span><span class="sxs-lookup"><span data-stu-id="4851f-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

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

