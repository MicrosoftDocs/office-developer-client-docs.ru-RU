---
title: Объект-контейнер (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702126"
---
# <a name="container-object-dao"></a><span data-ttu-id="ed0a1-102">Объект-контейнер (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed0a1-102">Container object (DAO)</span></span>

<span data-ttu-id="ed0a1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed0a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed0a1-104">Объект **контейнера** групп сходных типов объектов **документа** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed0a1-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="ed0a1-105">Remarks</span></span>

<span data-ttu-id="ed0a1-106">Каждый объект **базы данных** имеет коллекцию **контейнеров** , состоящую из встроенных объектов **контейнера** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-106">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects.</span></span> <span data-ttu-id="ed0a1-107">Приложения могут определять собственные типы документов и соответствующих контейнеров (Microsoft Access базами данных, ядро только); Тем не менее эти объекты может не всегда поддерживаться через DAO.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-107">Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="ed0a1-108">Некоторые из этих объектов **контейнера** определяются ядро базы данных Microsoft Access, в то время как другие пользователи могут быть определены с другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-108">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications.</span></span> <span data-ttu-id="ed0a1-109">В следующей таблице перечислены имя каждого объекта- **контейнера** определяется ядро базы данных Microsoft Access и тип информации о нем.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-109">The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ed0a1-110">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="ed0a1-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="ed0a1-111">Содержит сведения о</span><span class="sxs-lookup"><span data-stu-id="ed0a1-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ed0a1-112">Databases</span><span class="sxs-lookup"><span data-stu-id="ed0a1-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="ed0a1-113">Сохраненные баз данных</span><span class="sxs-lookup"><span data-stu-id="ed0a1-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ed0a1-114">таблицы;</span><span class="sxs-lookup"><span data-stu-id="ed0a1-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="ed0a1-115">Сохранить таблиц и запросов</span><span class="sxs-lookup"><span data-stu-id="ed0a1-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ed0a1-116">Relations</span><span class="sxs-lookup"><span data-stu-id="ed0a1-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="ed0a1-117">Сохраненные связей</span><span class="sxs-lookup"><span data-stu-id="ed0a1-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ed0a1-118">Не следует путать объекты **контейнеров** , перечисленных в предыдущей таблице с семействами с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-118">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name.</span></span> <span data-ttu-id="ed0a1-119">Баз данных **контейнер** объекта ссылается на все объекты сохраненного базы данных, но семейства **баз данных** относится только к объекты базы данных, которые открыты в конкретной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-119">The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="ed0a1-120">Каждый объект- **контейнер** имеет **документы** коллекцию, содержащую объекты **документов** , которые описывают экземпляры встроенные объекты типа, указанного в качестве **контейнера**.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-120">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**.</span></span> <span data-ttu-id="ed0a1-121">Объект **контейнера** обычно используется как промежуточных ссылка на сведения, приведенные в объект **Document** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-121">You typically use a **Container** object as an intermediate link to the information in the **Document** object.</span></span> <span data-ttu-id="ed0a1-122">Коллекция **контейнеров** можно также использовать настройки безопасности для всех объектов **документов** данного типа.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-122">You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="ed0a1-123">Существующий объект **контейнера** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="ed0a1-124">Используйте свойство **Name** возвращает предварительно определенное имя для объекта- **контейнера** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="ed0a1-125">Используйте свойство **владельца** или возвращает владельца объекта- **контейнера** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-125">Use the **Owner** property to set or return the owner of the **Container** object.</span></span> <span data-ttu-id="ed0a1-126">Для установки свойства **Owner** , необходимо иметь разрешения на запись для объекта- **контейнера** , а свойству необходимо присвоить имя существующего объекта **пользователя** или **группы** .</span><span class="sxs-lookup"><span data-stu-id="ed0a1-126">To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="ed0a1-127">Использование свойств **разрешения** и **имя пользователя** для настройки разрешений доступа для объекта **контейнера** ; любой объект **документа** , созданного в коллекции **документов** для объекта- **контейнера** наследует эти параметры разрешений доступа.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="ed0a1-128">Поскольку встроенные объекты **контейнеров** , не могут создавать новые объекты **контейнера** или удалять существующие.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="ed0a1-129">Для ссылки на объект **контейнера** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="ed0a1-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="ed0a1-130">**Контейнеры** (0)</span><span class="sxs-lookup"><span data-stu-id="ed0a1-130">**Containers**(0)</span></span>

- <span data-ttu-id="ed0a1-131">**Контейнеры** («*имя*»)</span><span class="sxs-lookup"><span data-stu-id="ed0a1-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="ed0a1-132">**Контейнеры**\!\[*имя*\]</span><span class="sxs-lookup"><span data-stu-id="ed0a1-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="ed0a1-133">Пример</span><span class="sxs-lookup"><span data-stu-id="ed0a1-133">Example</span></span>

<span data-ttu-id="ed0a1-134">В этом примере перечисляются коллекция **контейнеров** базы данных Northwind и коллекции **свойств** для каждого объекта- **контейнера** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ed0a1-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

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
