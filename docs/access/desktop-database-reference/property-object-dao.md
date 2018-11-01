---
title: Property Object (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50f7cc2b977b25602e8aec440796f105055a7437
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875636"
---
# <a name="property-object-dao"></a><span data-ttu-id="16364-102">Property Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="16364-102">Property Object (DAO)</span></span>


<span data-ttu-id="16364-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16364-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16364-104">Объект **Property** представляет характеристику встроенные или пользовательские объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="16364-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16364-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="16364-105">Remarks</span></span>

<span data-ttu-id="16364-106">Каждый объект DAO, за исключением объекты **подключения** и **Ошибка** содержит коллекцию **свойств** , которая имеет **свойство** объекты, соответствующий встроенных свойств этого объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="16364-106">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object.</span></span> <span data-ttu-id="16364-107">Пользователя можно определить объекты **Свойства** и добавьте их в коллекцию **свойств** некоторых объектов DAO.</span><span class="sxs-lookup"><span data-stu-id="16364-107">The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects.</span></span> <span data-ttu-id="16364-108">Эти объекты **свойство** (которые часто просто называются свойства) однозначно Создание характеристик этого экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="16364-108">These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="16364-109">Можно создать пользовательские свойства для следующих объектов:</span><span class="sxs-lookup"><span data-stu-id="16364-109">You can create user-defined properties for the following objects:</span></span>

  - <span data-ttu-id="16364-110">Объекты **базы данных**, **индекса**, **QueryDef**и **TableDef**</span><span class="sxs-lookup"><span data-stu-id="16364-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

  - <span data-ttu-id="16364-111">**Поля** объектов в коллекции **полей** **TableDef** и **QueryDef** объектов</span><span class="sxs-lookup"><span data-stu-id="16364-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="16364-112">Чтобы добавить пользовательские свойства, используйте метод **CreateProperty** для создания объекта **Свойства** с помощью уникальное **имя** свойства.</span><span class="sxs-lookup"><span data-stu-id="16364-112">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting.</span></span> <span data-ttu-id="16364-113">Установка свойств **типа** и **значения** для этого нового объекта **свойство** и затем добавить его в коллекцию **свойств** соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="16364-113">Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object.</span></span> <span data-ttu-id="16364-114">Объект, для которого требуется добавить пользовательские свойства уже должен быть добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="16364-114">The object to which you are adding the user-defined property must already be appended to a collection.</span></span> <span data-ttu-id="16364-115">Создание ссылок на объект пользовательские **Свойства** , который еще не была добавлена к коллекции **свойств** вызовет ошибку, как и добавление объект пользовательских **свойств** в коллекцию **свойств** , содержащую \*\* Свойство\*\* объект с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="16364-115">Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="16364-116">Пользовательские свойства можно удалить из коллекции **свойств** , но не смогут удалять встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="16364-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="16364-117">Объект пользовательских <STRONG>свойств</STRONG> сопоставляется только с определенный экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="16364-117">A user-defined <STRONG>Property</STRONG> object is associated only with the specific instance of an object.</span></span> <span data-ttu-id="16364-118">Свойство не определено для всех экземпляров объектов выбранного типа.</span><span class="sxs-lookup"><span data-stu-id="16364-118">The property isn't defined for all instances of objects of the selected type.</span></span></P>



<span data-ttu-id="16364-119">Коллекции **свойств** объекта можно использовать для перечисления встроенные и пользовательские свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="16364-119">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties.</span></span> <span data-ttu-id="16364-120">Не нужно знать заранее точно свойств, которые существуют или их характеристики (**имя** и **Тип** свойства), находятся в управлении ими.</span><span class="sxs-lookup"><span data-stu-id="16364-120">You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them.</span></span> <span data-ttu-id="16364-121">Тем не менее если вы попробуйте для чтения свойство только для записи, такими как свойство **пароль** объекта **рабочей области** или выполнить чтение или запись свойства в недопустимом контексте, такие как параметр свойства **Value** объекта **поля** в Коллекции **полей** объекта **TableDef** ошибка возникает.</span><span class="sxs-lookup"><span data-stu-id="16364-121">However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="16364-122">**Свойство** object также имеет четыре встроенных свойства.</span><span class="sxs-lookup"><span data-stu-id="16364-122">The **Property** object also has four built-in properties:</span></span>

  - <span data-ttu-id="16364-123">Свойство **Name** , **строка** , однозначно идентифицирующая свойство.</span><span class="sxs-lookup"><span data-stu-id="16364-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

  - <span data-ttu-id="16364-124">Свойство **Type** , **целое число** , определяющее тип данных свойства.</span><span class="sxs-lookup"><span data-stu-id="16364-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

  - <span data-ttu-id="16364-125">Свойство **Value** , **типа Variant** , содержащее значение свойства.</span><span class="sxs-lookup"><span data-stu-id="16364-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

  - <span data-ttu-id="16364-126">**Inherited** свойство **типа Boolean** , указывающее, является ли свойство наследуется от другого объекта.</span><span class="sxs-lookup"><span data-stu-id="16364-126">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object.</span></span> <span data-ttu-id="16364-127">Например объект **поля** в коллекцию **полей** объекта **набора записей** могут наследовать свойства базового объекта **TableDef** или **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="16364-127">For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="16364-128">Для ссылки на объект встроенных **свойств** в семействе сайтов, с его порядковый номер или **его свойства Name** , можно используйте любой из следующих форм синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="16364-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

  - <span data-ttu-id="16364-129">\* Объект \***. Свойства**(0)</span><span class="sxs-lookup"><span data-stu-id="16364-129">\*object\***.Properties**(0)</span></span>

  - <span data-ttu-id="16364-130">\*объект \***. Свойства**(»\* имя \*»)</span><span class="sxs-lookup"><span data-stu-id="16364-130">*object\***.Properties**("* name\*")</span></span>

  - <span data-ttu-id="16364-131">\*объект \***. Свойства**\!\* имя \*\]</span><span class="sxs-lookup"><span data-stu-id="16364-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="16364-132">Для встроенных свойств можно также используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="16364-132">For a built-in property, you can also use this syntax:</span></span>

  - <span data-ttu-id="16364-133">*объект*. *имя*</span><span class="sxs-lookup"><span data-stu-id="16364-133">*object*.*name*</span></span>


> [!NOTE]
> <P><span data-ttu-id="16364-134">Пользовательские свойства необходимо использовать полный <EM>объект</EM><STRONG>. Свойства</STRONG>синтаксис («<EM>имя</EM>»).</span><span class="sxs-lookup"><span data-stu-id="16364-134">For a user-defined property, you must use the full <EM>object</EM><STRONG>.Properties</STRONG>("<EM>name</EM>") syntax.</span></span></P>



<span data-ttu-id="16364-135">С помощью одной синтаксиса форм можно найти в свойство **Value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="16364-135">With the same syntax forms, you can also refer to the **Value** property of a **Property** object.</span></span> <span data-ttu-id="16364-136">Контекст ссылки определяет, будет ли вы ссылаетесь на объект **свойств** , самого или свойство **Value** объекта **Property** .</span><span class="sxs-lookup"><span data-stu-id="16364-136">The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

