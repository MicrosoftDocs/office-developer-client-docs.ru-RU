---
title: Элементы Outlook и полей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 605fab0f-c045-4d2b-a2da-447a111f66a9
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 71c67c37cc4f9cd3ddd7a55c37c4ebd6ddd35cfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810083"
---
# <a name="outlook-items-and-fields"></a><span data-ttu-id="fca60-103">Элементы Outlook и полей</span><span class="sxs-lookup"><span data-stu-id="fca60-103">Outlook Items and Fields</span></span>

  
  
<span data-ttu-id="fca60-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fca60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fca60-105">Microsoft Outlook предоставляет типы элементов, которые специализируются функциональные возможности (, например почтовых элементов, встречи, контакты, задачи и заметки).</span><span class="sxs-lookup"><span data-stu-id="fca60-105">Microsoft Outlook provides item types that are specialized for their functionality (for example, mail items, appointments, contacts, tasks, and notes).</span></span> <span data-ttu-id="fca60-106">Outlook предоставляет стандартных полей для каждого типа элемента, обычно называемую встроенных полей.</span><span class="sxs-lookup"><span data-stu-id="fca60-106">Outlook provides standard fields for each type of item, commonly referred to as built-in fields.</span></span> <span data-ttu-id="fca60-107">Outlook позволяет пользователям создавать настраиваемые поля, обычно называемую пользовательских полей.</span><span class="sxs-lookup"><span data-stu-id="fca60-107">Outlook also allows users to create custom fields, commonly referred to as user-defined fields.</span></span> <span data-ttu-id="fca60-108">В каждом поле связан с типом данных и значением.</span><span class="sxs-lookup"><span data-stu-id="fca60-108">Each field is associated with a data type and a value.</span></span> <span data-ttu-id="fca60-109">Примеры типов данных, **валюты**, **Даты и времени**, **длительность**, **целое число**, **ключевые слова**и **текст**.</span><span class="sxs-lookup"><span data-stu-id="fca60-109">Examples of data types are **Currency**, **Date/Time**, **Duration**, **Integer**, **Keywords**, and **Text**.</span></span> <span data-ttu-id="fca60-110">Пользователи могут определять настраиваемые поля с помощью конструктора форм в Outlook.</span><span class="sxs-lookup"><span data-stu-id="fca60-110">Users can define custom fields by using the Forms Designer in Outlook.</span></span>
  
<span data-ttu-id="fca60-111">На уровне программирования каждого элемента представлен объектом [IMessage](imessageimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="fca60-111">At the programmability level, each item is represented by an [IMessage](imessageimapiprop.md) object.</span></span> <span data-ttu-id="fca60-112">В каждом поле пользовательских связан с определения поля и значения.</span><span class="sxs-lookup"><span data-stu-id="fca60-112">Each user-defined field is associated with a field definition and a value.</span></span> 
  
### <a name="field-definition"></a><span data-ttu-id="fca60-113">Определение поля</span><span class="sxs-lookup"><span data-stu-id="fca60-113">Field Definition</span></span>

<span data-ttu-id="fca60-114">Определение поля включает в себя имя, тип данных и другие сведения о поле.</span><span class="sxs-lookup"><span data-stu-id="fca60-114">A field definition includes the name, data type, and other information about the field.</span></span> <span data-ttu-id="fca60-115">Для каждого элемента Outlook хранятся определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="fca60-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="fca60-116">Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известных как [Определение свойства](propertydefinition-stream-structure.md) , которое содержит определения полей.</span><span class="sxs-lookup"><span data-stu-id="fca60-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md) that contains the field definitions.</span></span> <span data-ttu-id="fca60-117">Дополнительные сведения о потоке структуры для определения полей можно [Структур потока](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="fca60-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
### <a name="field-value"></a><span data-ttu-id="fca60-118">Значение поля</span><span class="sxs-lookup"><span data-stu-id="fca60-118">Field Value</span></span>

<span data-ttu-id="fca60-119">Каждый пользовательские поля элемента имеет значение, которая хранится в соответствующем именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="fca60-119">Each user-defined field of an item has a value that is stored in a corresponding named property.</span></span> <span data-ttu-id="fca60-120">Именованные свойства PS_PUBLIC_STRINGS набор свойств и его строку знаков Юникод в качестве имени свойства.</span><span class="sxs-lookup"><span data-stu-id="fca60-120">That named property is in the PS_PUBLIC_STRINGS property set, and has a Unicode character string as the property name.</span></span> <span data-ttu-id="fca60-121">Тип данных свойства соответствует типа поля.</span><span class="sxs-lookup"><span data-stu-id="fca60-121">The data type of the property corresponds to the type of the field.</span></span> <span data-ttu-id="fca60-122">Если свойство не существует в объекте **IMessage** , Outlook предполагается значение разумные по умолчанию для свойства.</span><span class="sxs-lookup"><span data-stu-id="fca60-122">If the property is not present in the **IMessage** object, Outlook assumes a reasonable default value for the property.</span></span> <span data-ttu-id="fca60-123">Например для типа string, Outlook предполагается пустая строка, если свойство не указан.</span><span class="sxs-lookup"><span data-stu-id="fca60-123">For example, for a string type, Outlook assumes an empty string if the property is not present.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fca60-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fca60-124">See also</span></span>



[<span data-ttu-id="fca60-125">Добавьте определение для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="fca60-125">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="fca60-126">Определение свойства потока образца</span><span class="sxs-lookup"><span data-stu-id="fca60-126">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="fca60-127">Поток структуры</span><span class="sxs-lookup"><span data-stu-id="fca60-127">Stream Structures</span></span>](stream-structures.md)
  
[<span data-ttu-id="fca60-128">Определение свойства потока структуры</span><span class="sxs-lookup"><span data-stu-id="fca60-128">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
  
[<span data-ttu-id="fca60-129">Структура FieldDefinition потока</span><span class="sxs-lookup"><span data-stu-id="fca60-129">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
  
[<span data-ttu-id="fca60-130">Структура SkipBlock потока</span><span class="sxs-lookup"><span data-stu-id="fca60-130">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
  
[<span data-ttu-id="fca60-131">Структура FirstSkipBlockContent потока</span><span class="sxs-lookup"><span data-stu-id="fca60-131">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
  
[<span data-ttu-id="fca60-132">Структура PackedAnsiString потока</span><span class="sxs-lookup"><span data-stu-id="fca60-132">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
  
[<span data-ttu-id="fca60-133">Структура PackedUnicodeString потока</span><span class="sxs-lookup"><span data-stu-id="fca60-133">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

