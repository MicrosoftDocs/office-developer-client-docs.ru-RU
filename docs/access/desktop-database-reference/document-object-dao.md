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
# <a name="document-object-dao"></a><span data-ttu-id="60e33-102">Объект Document (DAO)</span><span class="sxs-lookup"><span data-stu-id="60e33-102">Document object (DAO)</span></span>

<span data-ttu-id="60e33-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60e33-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60e33-104">Объект **Document** включает сведения об одном экземпляре объекта.</span><span class="sxs-lookup"><span data-stu-id="60e33-104">A **Document** object includes information about one instance of an object.</span></span> <span data-ttu-id="60e33-105">Объект может быть базой данных, сохраненной таблицей, запросом или отношением (только базы данных ядра СУБД Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="60e33-105">The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="60e33-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="60e33-106">Remarks</span></span>

<span data-ttu-id="60e33-107">Каждый объект **Container** содержит коллекцию **Documents** , содержащую объекты **Document** , которые описывают экземпляры встроенных объектов типа, указанного в контейнере \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="60e33-107">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="60e33-108">В следующей таблице перечислены типы объектов, описанных в каждом **документе** , имя его объекта **Container** и тип информационного **документа** .</span><span class="sxs-lookup"><span data-stu-id="60e33-108">The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60e33-109">Document</span><span class="sxs-lookup"><span data-stu-id="60e33-109">Document</span></span></p></th>
<th><p><span data-ttu-id="60e33-110">Container</span><span class="sxs-lookup"><span data-stu-id="60e33-110">Container</span></span></p></th>
<th><p><span data-ttu-id="60e33-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="60e33-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60e33-112">Database</span><span class="sxs-lookup"><span data-stu-id="60e33-112">Database</span></span></p></td>
<td><p><span data-ttu-id="60e33-113">Базы данных</span><span class="sxs-lookup"><span data-stu-id="60e33-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="60e33-114">Сохраненная база данных</span><span class="sxs-lookup"><span data-stu-id="60e33-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60e33-115">Таблица или запрос</span><span class="sxs-lookup"><span data-stu-id="60e33-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="60e33-116">Tables</span><span class="sxs-lookup"><span data-stu-id="60e33-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="60e33-117">Сохраненная таблица или запрос</span><span class="sxs-lookup"><span data-stu-id="60e33-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60e33-118">Отношение</span><span class="sxs-lookup"><span data-stu-id="60e33-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="60e33-119">Relations</span><span class="sxs-lookup"><span data-stu-id="60e33-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="60e33-120">Сохраненная связь</span><span class="sxs-lookup"><span data-stu-id="60e33-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="60e33-121">Не путайте объекты **контейнера** , перечисленные в предыдущей таблице, с коллекциями с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="60e33-121">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="60e33-122">Объект **контейнера** баз данных относится ко всем сохраненным объектам базы данных, но семейство **баз данных** относится только к объектам базы данных, открытым в определенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="60e33-122">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="60e33-123">Объект **Document** позволяет:</span><span class="sxs-lookup"><span data-stu-id="60e33-123">With a **Document** object, you can:</span></span>

- <span data-ttu-id="60e33-124">Используйте свойство **Name** , чтобы возвратить имя, которое пользователь или ядро СУБД Microsoft Access предоставило объекту при его создании.</span><span class="sxs-lookup"><span data-stu-id="60e33-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

- <span data-ttu-id="60e33-125">С помощью свойства **Container** можно возвратить имя объекта **контейнера** , содержащего объект **Document** .</span><span class="sxs-lookup"><span data-stu-id="60e33-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

- <span data-ttu-id="60e33-126">Используйте свойство **owner** , чтобы задать или вернуть владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="60e33-126">Use the **Owner** property to set or return the owner of the object.</span></span> <span data-ttu-id="60e33-127">Чтобы задать свойство **owner** , необходимо иметь разрешение на запись для объекта **Document** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="60e33-127">To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="60e33-128">Используйте свойства **username** и **Permissions** , чтобы задать или вернуть разрешения на доступ к объекту для пользователя или группы.</span><span class="sxs-lookup"><span data-stu-id="60e33-128">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object.</span></span> <span data-ttu-id="60e33-129">Чтобы задать эти свойства, необходимо иметь разрешение на запись для объекта **Document** , а свойству **username** необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="60e33-129">To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="60e33-130">Используйте свойства **DateCreated** и **ластупдатед** , чтобы получить дату и время создания и последнего изменения объекта **документа** .</span><span class="sxs-lookup"><span data-stu-id="60e33-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="60e33-131">Так как объект **Document** соответствует существующему объекту, вы не можете создавать новые объекты **документа** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="60e33-131">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones.</span></span> <span data-ttu-id="60e33-132">Чтобы сослаться на объект **Document** в коллекции по его порядковому номеру или по его свойству **Name** , используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="60e33-132">To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="60e33-133">**Документы** нуль</span><span class="sxs-lookup"><span data-stu-id="60e33-133">**Documents**(0)</span></span>

- <span data-ttu-id="60e33-134">**Документы** ("*имя*")</span><span class="sxs-lookup"><span data-stu-id="60e33-134">**Documents**("*name*")</span></span>

- <span data-ttu-id="60e33-135">\*\*\*\*\!\[*Имя* документа\]</span><span class="sxs-lookup"><span data-stu-id="60e33-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="60e33-136">Пример</span><span class="sxs-lookup"><span data-stu-id="60e33-136">Example</span></span>

<span data-ttu-id="60e33-137">В этом примере выполняется перечисление коллекции **Documents** контейнера Tables, после чего выполняется перечисление коллекции **свойств** первого объекта **Document** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="60e33-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

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

<span data-ttu-id="60e33-138">В этом примере используются свойства **owner** и **системдб** для отображения владельцев множества объектов **Document** .</span><span class="sxs-lookup"><span data-stu-id="60e33-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

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

