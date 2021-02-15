---
title: Объект Property (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301192"
---
# <a name="property-object-dao"></a><span data-ttu-id="73263-102">Объект Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="73263-102">Property object (DAO)</span></span>

<span data-ttu-id="73263-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73263-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73263-104">Объект **Property** представляет встроенную или определяемую пользователем характеристику объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="73263-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73263-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="73263-105">Remarks</span></span>

<span data-ttu-id="73263-106">Каждый объект DAO, кроме объектов **Connection** и **Error,** содержит коллекцию **свойств,** которая содержит объекты **Property,** соответствующие встроенным свойствам этого объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="73263-106">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object.</span></span> <span data-ttu-id="73263-107">Пользователь также может определить **объекты Property** и примедить их в коллекцию **свойств** некоторых объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="73263-107">The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects.</span></span> <span data-ttu-id="73263-108">Эти **объекты** Property (которые часто называются просто свойствами) уникальным образом характеризуют этот экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="73263-108">These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="73263-109">Можно создать пользовательские свойства для следующих объектов:</span><span class="sxs-lookup"><span data-stu-id="73263-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="73263-110">**Объекты Database,** **Index,** **QueryDef** и **TableDef**</span><span class="sxs-lookup"><span data-stu-id="73263-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="73263-111">**Объекты** field в коллекциях **Fields** объектов **QueryDef** **и TableDef**</span><span class="sxs-lookup"><span data-stu-id="73263-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="73263-112">Чтобы добавить определяемое пользователем свойство, используйте метод **CreateProperty,** чтобы создать объект **Property** с уникальным параметром свойства **Name.**</span><span class="sxs-lookup"><span data-stu-id="73263-112">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting.</span></span> <span data-ttu-id="73263-113">Установите свойства **Type** и **Value** нового объекта **Property,** а затем append его в коллекцию **свойств** соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="73263-113">Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object.</span></span> <span data-ttu-id="73263-114">Объект, к которому добавляется пользовательское свойство, уже должен быть добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="73263-114">The object to which you are adding the user-defined property must already be appended to a collection.</span></span> <span data-ttu-id="73263-115">Ссылка на пользовательский объект **Property,** который еще не был придан коллекции **свойств,** приведет к ошибке, так же  как и к коллекции **свойств,** содержащей объект **Property** с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="73263-115">Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="73263-116">Вы можете удалить пользовательские свойства из коллекции **Properties,** но не можете удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="73263-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="73263-117">Пользовательский объект **Property** связан только с определенным экземпляром объекта.</span><span class="sxs-lookup"><span data-stu-id="73263-117">A user-defined **Property** object is associated only with the specific instance of an object.</span></span> <span data-ttu-id="73263-118">Свойство определяется не для всех экземпляров объектов выбранного типа.</span><span class="sxs-lookup"><span data-stu-id="73263-118">The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="73263-119">Вы можете использовать коллекцию **свойств** объекта для нумерации встроенных и пользовательских свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="73263-119">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties.</span></span> <span data-ttu-id="73263-120">Вам не нужно точно знать, какие свойства существуют или каковы их характеристики (свойства **name** и **Type)** для управления ими.</span><span class="sxs-lookup"><span data-stu-id="73263-120">You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them.</span></span> <span data-ttu-id="73263-121">Однако если попытаться прочитать свойство, доступное только для записи, например свойство **Password** объекта **Workspace,** или попытаться прочитать или записать свойство в недопустимом контексте, например при настройке свойства **Value** объекта **Field** в коллекции **Fields** объекта **TableDef,** произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="73263-121">However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="73263-122">У **объекта Property** также есть четыре встроенных свойства:</span><span class="sxs-lookup"><span data-stu-id="73263-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="73263-123">Свойство **Name,** **строка,** однозначно определяя свойство.</span><span class="sxs-lookup"><span data-stu-id="73263-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="73263-124">Свойство **Type,** **integer,** которое указывает тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="73263-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="73263-125">Свойство **Value,** **Variant,** которое содержит параметр свойства.</span><span class="sxs-lookup"><span data-stu-id="73263-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="73263-126">Свойство **Inherited,** **boolean,** которое указывает, наследуется ли свойство от другого объекта.</span><span class="sxs-lookup"><span data-stu-id="73263-126">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object.</span></span> <span data-ttu-id="73263-127">Например, объект **Field** в коллекции **Fields** объекта **Recordset** может наследовать свойства от объекта **TableDef** или **QueryDef.**</span><span class="sxs-lookup"><span data-stu-id="73263-127">For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="73263-128">Чтобы сослаться на встроенный объект **Property** в коллекции по его порядковому номеру или по его свойству **Name,** используйте любую из следующих синтаксис-форм:</span><span class="sxs-lookup"><span data-stu-id="73263-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="73263-129">\*object\***. Свойства**(0)</span><span class="sxs-lookup"><span data-stu-id="73263-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="73263-130">*object\***. Properties**("* name\*")</span><span class="sxs-lookup"><span data-stu-id="73263-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="73263-131">*object\*\*\*. Имя свойства*\*\* \! \[\*\]</span><span class="sxs-lookup"><span data-stu-id="73263-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="73263-132">Для встроенного свойства можно также использовать такой синтаксис:</span><span class="sxs-lookup"><span data-stu-id="73263-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="73263-133">*object .* *name*</span><span class="sxs-lookup"><span data-stu-id="73263-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="73263-134">Для определяемого пользователем свойства необходимо использовать полный *объект\*\*\*. Синтаксис*\*\* свойств (" имя\*").</span><span class="sxs-lookup"><span data-stu-id="73263-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="73263-135">С помощью тех же форм синтаксиса можно также ссылаться на свойство **Value** объекта **Property.**</span><span class="sxs-lookup"><span data-stu-id="73263-135">With the same syntax forms, you can also refer to the **Value** property of a **Property** object.</span></span> <span data-ttu-id="73263-136">Контекст ссылки определяет, ссылается ли вы на сам объект **Property** или свойство **Value** объекта **Property.**</span><span class="sxs-lookup"><span data-stu-id="73263-136">The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

