---
title: Элементы и поля Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b40752d4a5f445368752ad4caf5c919f6e0ce27b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409120"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="816ea-103">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="816ea-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="816ea-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="816ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="816ea-105">Microsoft Outlook предоставляет типы элементов, специализированные для их функциональности (например, почтовые элементы, встречи, контакты, задачи и заметки).</span><span class="sxs-lookup"><span data-stu-id="816ea-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="816ea-106">Outlook предоставляет стандартные поля для каждого типа элемента, обычно именуемого встроенными полями.</span><span class="sxs-lookup"><span data-stu-id="816ea-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="816ea-107">Outlook также позволяет пользователям создавать настраиваемые поля, которые обычно называются пользовательскими полями.</span><span class="sxs-lookup"><span data-stu-id="816ea-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="816ea-108">Каждое поле связано с типом данных и значением.</span><span class="sxs-lookup"><span data-stu-id="816ea-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="816ea-109">Примеры типов данных: **"Валюта",** **"Дата/время",** **"Длительность",** **"Integer",** **"Ключевые слова"** и **"Текст".**</span><span class="sxs-lookup"><span data-stu-id="816ea-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="816ea-110">Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.</span><span class="sxs-lookup"><span data-stu-id="816ea-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="816ea-111">На уровне программируемости каждый элемент представлен объектом [IMessage.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="816ea-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="816ea-112">Каждое пользовательское поле связано с определением поля и значением.</span><span class="sxs-lookup"><span data-stu-id="816ea-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="816ea-113">Определение поля</span><span class="sxs-lookup"><span data-stu-id="816ea-113">Field Definition</span></span>

<span data-ttu-id="816ea-114">Определение поля включает имя, тип данных и другие сведения о поле.</span><span class="sxs-lookup"><span data-stu-id="816ea-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="816ea-115">Для каждого элемента Outlook сохраняет определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего **объекта IMessage.**</span><span class="sxs-lookup"><span data-stu-id="816ea-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="816ea-116">Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известный как [PropertyDefinition,](propertydefinition-stream-structure.md) содержащий определения полей.</span><span class="sxs-lookup"><span data-stu-id="816ea-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="816ea-117">Дополнительные сведения о структурах потоков для определений полей см. в [подстройки Stream.](stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="816ea-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="816ea-118">Значение поля</span><span class="sxs-lookup"><span data-stu-id="816ea-118">Field Value</span></span>

<span data-ttu-id="816ea-119">Каждое определяемого пользователем поле элемента имеет значение, которое хранится в соответствующем именоваемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="816ea-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="816ea-120">Это именоватое свойство находится в PS_PUBLIC_STRINGS свойства и имеет строку символов Юникода в качестве имени свойства.</span><span class="sxs-lookup"><span data-stu-id="816ea-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="816ea-121">Тип данных свойства соответствует типу поля.</span><span class="sxs-lookup"><span data-stu-id="816ea-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="816ea-122">Если свойство не присутствует в объекте **IMessage,** Outlook принимает разумное значение по умолчанию для свойства.</span><span class="sxs-lookup"><span data-stu-id="816ea-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="816ea-123">Например, для типа строки Outlook предполагает пустую строку, если свойства нет.</span><span class="sxs-lookup"><span data-stu-id="816ea-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="816ea-124">См. также</span><span class="sxs-lookup"><span data-stu-id="816ea-124">See also</span></span>



[<span data-ttu-id="816ea-125">Добавление определения для нового поля User-Defined</span><span class="sxs-lookup"><span data-stu-id="816ea-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="816ea-126">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="816ea-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="816ea-127">Структуры потоков</span><span class="sxs-lookup"><span data-stu-id="816ea-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="816ea-128">Структура потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="816ea-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="816ea-129">Структура потока FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="816ea-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="816ea-130">Структура потока SkipBlock</span><span class="sxs-lookup"><span data-stu-id="816ea-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="816ea-131">Структура потока FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="816ea-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="816ea-132">Структура потока PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="816ea-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="816ea-133">Структура потока PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="816ea-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

