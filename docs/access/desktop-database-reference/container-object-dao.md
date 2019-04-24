---
title: Объект Container (DAO)
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
# <a name="container-object-dao"></a><span data-ttu-id="41b8b-102">Объект Container (DAO)</span><span class="sxs-lookup"><span data-stu-id="41b8b-102">Container object (DAO)</span></span>

<span data-ttu-id="41b8b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41b8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41b8b-104">Объект **Container** группирует похожие типы объектов **документа** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="41b8b-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="41b8b-105">Remarks</span></span>

<span data-ttu-id="41b8b-106">Каждый объект **базы данных** содержит коллекцию **Containers** , состоящую из встроенных объектов **контейнера** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="41b8b-107">Приложения могут определять собственные типы документов и соответствующие контейнеры (только базы данных ядра СУБД Microsoft Access); Тем не менее, эти объекты не всегда поддерживаются с помощью DAO.</span><span class="sxs-lookup"><span data-stu-id="41b8b-107">Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="41b8b-108">Некоторые из этих объектов **Container** определены ядром СУБД Microsoft Access, в то время как другие могут определять другие приложения.</span><span class="sxs-lookup"><span data-stu-id="41b8b-108">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span> <span data-ttu-id="41b8b-109">В следующей таблице приведены имена всех объектов **Container** , определенных ядром СУБД Microsoft Access, и типы данных, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="41b8b-109">The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41b8b-110">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="41b8b-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="41b8b-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="41b8b-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41b8b-112">Databases</span><span class="sxs-lookup"><span data-stu-id="41b8b-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="41b8b-113">Сохраненные базы данных</span><span class="sxs-lookup"><span data-stu-id="41b8b-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41b8b-114">Tables</span><span class="sxs-lookup"><span data-stu-id="41b8b-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="41b8b-115">Сохраненные таблицы и запросы</span><span class="sxs-lookup"><span data-stu-id="41b8b-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41b8b-116">Relations</span><span class="sxs-lookup"><span data-stu-id="41b8b-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="41b8b-117">Сохраненные связи</span><span class="sxs-lookup"><span data-stu-id="41b8b-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="41b8b-118">Не путайте объекты **контейнера** , перечисленные в предыдущей таблице, с коллекциями с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="41b8b-118">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="41b8b-119">Объект **контейнера** баз данных относится ко всем сохраненным объектам базы данных, но семейство **баз данных** относится только к объектам базы данных, открытым в определенной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="41b8b-119">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="41b8b-120">Каждый объект **Container** содержит коллекцию **Documents** , содержащую объекты **Document** , которые описывают экземпляры встроенных объектов типа, указанного в контейнере \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="41b8b-120">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="41b8b-121">Как правило, объект **Container** используется в качестве промежуточной ссылки на информацию в объекте **Document** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-121">You typically use a **Container** object as an intermediate link to the information in the **Document** object.</span></span> <span data-ttu-id="41b8b-122">Вы также можете использовать коллекцию **Containers** , чтобы задать безопасность для всех объектов **документа** определенного типа.</span><span class="sxs-lookup"><span data-stu-id="41b8b-122">You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="41b8b-123">С помощью существующего объекта **Container** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="41b8b-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="41b8b-124">Используйте свойство **Name** , чтобы возвратить предварительно определенное имя объекта **Container** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="41b8b-125">Используйте свойство **owner** , чтобы задать или вернуть владельца объекта **Container** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-125">Use the **Owner** property to set or return the owner of the **Container** object.</span></span> <span data-ttu-id="41b8b-126">Чтобы задать свойство **owner** , необходимо иметь разрешение на запись для объекта **Container** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="41b8b-126">To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="41b8b-127">Используйте свойства **Permissions** и **username** , чтобы задать разрешения доступа для объекта **Container** ; любой объект **документа** , созданный в коллекции **Documents** объекта **Container** , наследует эти параметры разрешений на доступ.</span><span class="sxs-lookup"><span data-stu-id="41b8b-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="41b8b-128">Так как объекты **контейнеров** являются встроенными, вы не можете создавать новые объекты- **контейнеры** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="41b8b-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="41b8b-129">Чтобы сослаться на объект **контейнера** в коллекции по его порядковому номеру или по значению свойства **Name** , используйте любую из следующих синтаксических форм:</span><span class="sxs-lookup"><span data-stu-id="41b8b-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="41b8b-130">**Контейнеры** нуль</span><span class="sxs-lookup"><span data-stu-id="41b8b-130">**Containers**(0)</span></span>

- <span data-ttu-id="41b8b-131">**Контейнеры** ("*имя*")</span><span class="sxs-lookup"><span data-stu-id="41b8b-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="41b8b-132">\*\*\*\*\!\[*Имя* контейнера\]</span><span class="sxs-lookup"><span data-stu-id="41b8b-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="41b8b-133">Пример</span><span class="sxs-lookup"><span data-stu-id="41b8b-133">Example</span></span>

<span data-ttu-id="41b8b-134">В этом примере показано, как перечислить коллекцию **контейнеров** базы данных Northwind и коллекцию **свойств** каждого объекта **Container** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="41b8b-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

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
