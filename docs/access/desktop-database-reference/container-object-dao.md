---
title: Контейнерный объект (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295634"
---
# <a name="container-object-dao"></a><span data-ttu-id="21bb7-102">Контейнерный объект (DAO)</span><span class="sxs-lookup"><span data-stu-id="21bb7-102">Container object (DAO)</span></span>

<span data-ttu-id="21bb7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21bb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21bb7-104">Объект **Контейнера** объединяет аналогичные типы **объектов Document.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bb7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="21bb7-105">Remarks</span></span>

<span data-ttu-id="21bb7-106">Каждый **объект Базы** данных имеет коллекцию **контейнеров,** состоящую из встроенных **контейнерных** объектов.</span><span class="sxs-lookup"><span data-stu-id="21bb7-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="21bb7-107">Приложения могут определять собственные типы документов и соответствующие контейнеры (только базы данных баз данных Microsoft Access); однако эти объекты не всегда могут поддерживаться с помощью DAO.</span><span class="sxs-lookup"><span data-stu-id="21bb7-107">Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="21bb7-108">Некоторые из этих **объектов контейнера** определяются механизмом базы данных Microsoft Access, а другие могут быть определены другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="21bb7-108">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span> <span data-ttu-id="21bb7-109">В следующей таблице перечислены имя каждого объекта **контейнера,** определенного движком базы данных Microsoft Access, и тип информации, которая в нем содержится.</span><span class="sxs-lookup"><span data-stu-id="21bb7-109">The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21bb7-110">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="21bb7-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="21bb7-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="21bb7-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21bb7-112">Databases</span><span class="sxs-lookup"><span data-stu-id="21bb7-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="21bb7-113">Сохраненные базы данных</span><span class="sxs-lookup"><span data-stu-id="21bb7-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21bb7-114">Таблицы</span><span class="sxs-lookup"><span data-stu-id="21bb7-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="21bb7-115">Сохраненные таблицы и запросы</span><span class="sxs-lookup"><span data-stu-id="21bb7-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21bb7-116">Relations</span><span class="sxs-lookup"><span data-stu-id="21bb7-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="21bb7-117">Сохраненные отношения</span><span class="sxs-lookup"><span data-stu-id="21bb7-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="21bb7-118">Не путайте **объекты Container,** перечисленные в предыдущей таблице, с коллекциями с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="21bb7-118">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="21bb7-119">Объект Контейнера **баз** данных относится к всем сохраненным объектам базы данных, но коллекция **Баз** данных относится только к объектам баз данных, которые открыты в определенном рабочем пространстве.</span><span class="sxs-lookup"><span data-stu-id="21bb7-119">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="21bb7-120">Каждый **объект Контейнер** имеет коллекцию **Документов,** содержащую объекты **Document,** описывая экземпляры встроенных объектов типа, указанного **контейнером.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-120">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="21bb7-121">Обычно объект **Container** используется в качестве промежуточной ссылки на сведения в **объекте Document.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-121">You typically use a **Container** object as an intermediate link to the information in the **Document** object.</span></span> <span data-ttu-id="21bb7-122">Вы также можете использовать коллекцию **Контейнеры,** чтобы установить безопасность для всех объектов **Document** того или иного типа.</span><span class="sxs-lookup"><span data-stu-id="21bb7-122">You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="21bb7-123">С существующим **объектом Контейнер** можно:</span><span class="sxs-lookup"><span data-stu-id="21bb7-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="21bb7-124">Чтобы **вернуть** заранее задав имя объекта Container, используйте **свойство Name.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="21bb7-125">Используйте свойство **Owner,** чтобы установить или вернуть владельца **объекта Container.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-125">Use the **Owner** property to set or return the owner of the **Container** object.</span></span> <span data-ttu-id="21bb7-126">Чтобы установить свойство **Owner,** необходимо иметь разрешение на написание объекта **Container,** а также установить его имя существующего объекта **User** или **Group.**</span><span class="sxs-lookup"><span data-stu-id="21bb7-126">To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="21bb7-127">Используйте свойства **Permissions** и **UserName** для набора разрешений доступа для **объекта Контейнер;** любой **объект Document,** созданный в коллекции **Документов** объекта **Container,** наследует эти параметры разрешений доступа.</span><span class="sxs-lookup"><span data-stu-id="21bb7-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="21bb7-128">Так **как объекты Container** встроены, нельзя создавать новые объекты **контейнера** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="21bb7-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="21bb7-129">Чтобы сослаться на объект **Container** в коллекции по его порядковому номеру или по параметру свойства **Name,** используйте любую из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="21bb7-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="21bb7-130">**Контейнеры**(0)</span><span class="sxs-lookup"><span data-stu-id="21bb7-130">**Containers**(0)</span></span>

- <span data-ttu-id="21bb7-131">\**Контейнеры\*\*\*("имя")*</span><span class="sxs-lookup"><span data-stu-id="21bb7-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="21bb7-132">**Контейнеры** \! \[ *имя*\]</span><span class="sxs-lookup"><span data-stu-id="21bb7-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="21bb7-133">Пример</span><span class="sxs-lookup"><span data-stu-id="21bb7-133">Example</span></span>

<span data-ttu-id="21bb7-134">В этом примере содержится коллекция **контейнеров** базы данных Northwind и коллекция **свойств** каждого объекта **Контейнера** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="21bb7-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
