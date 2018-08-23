---
title: Каноническое свойство PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a584c6beec0f06ab4cc6bd95f4611d1f30189a8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595155"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="efba9-103">Каноническое свойство PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="efba9-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="efba9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efba9-105">Содержит имя, тип данных и другие сведения о пользовательских полей.</span><span class="sxs-lookup"><span data-stu-id="efba9-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="efba9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="efba9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="efba9-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="efba9-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="efba9-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="efba9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="efba9-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="efba9-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="efba9-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="efba9-110">Data type:</span></span>  <br/> |<span data-ttu-id="efba9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="efba9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="efba9-112">Область:</span><span class="sxs-lookup"><span data-stu-id="efba9-112">Area:</span></span>  <br/> |<span data-ttu-id="efba9-113">Папки MAPI</span><span class="sxs-lookup"><span data-stu-id="efba9-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efba9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="efba9-114">Remarks</span></span>

<span data-ttu-id="efba9-115">Для каждого элемента Outlook хранятся определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="efba9-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="efba9-116">Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известных как [Определение свойства](propertydefinition-stream-structure.md), который содержит определения полей.</span><span class="sxs-lookup"><span data-stu-id="efba9-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="efba9-117">Дополнительные сведения о потоке структуры для определения полей можно [Структур потока](stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="efba9-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="efba9-118">Для каждой папки Outlook хранятся определения всех пользовательских полей в эту папку в свойстве **PidTagUserFields** сообщения связанный класс сообщения IPC.MS. REN. USERFIELDS - каждой папки, которые, как содержать не более одной сообщение в таблице связанное содержимое этого класса.</span><span class="sxs-lookup"><span data-stu-id="efba9-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="efba9-119">Набор пользовательских полей в папке могут не соответствовать обязательно наборы пользовательских полей в каждой из его элементы.</span><span class="sxs-lookup"><span data-stu-id="efba9-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="efba9-120">Набор пользовательских полей в папке отображается в разных местах пользовательского интерфейса Outlook, такие как Выбор поля адреса папки.</span><span class="sxs-lookup"><span data-stu-id="efba9-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="efba9-121">Свойство **PidTagUserFields** сообщение содержит двоичный поток **FolderUserFields**, который содержит определения полей папки.</span><span class="sxs-lookup"><span data-stu-id="efba9-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="efba9-122">Дополнительные сведения о структуре потока для определения полей папки можно [Потока структуры папок полей](folder-fields-stream-structures.md) и [Пример FolderUserFields потока](folderuserfields-stream-sample.md).</span><span class="sxs-lookup"><span data-stu-id="efba9-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="efba9-123">Заголовок раздела</span><span class="sxs-lookup"><span data-stu-id="efba9-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="efba9-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="efba9-124">Protocol specifications</span></span>

<span data-ttu-id="efba9-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="efba9-125">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="efba9-126">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="efba9-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="efba9-127">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="efba9-127">Header files</span></span>

<span data-ttu-id="efba9-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="efba9-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="efba9-129">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="efba9-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="efba9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="efba9-130">See also</span></span>



[<span data-ttu-id="efba9-131">Поля и элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="efba9-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="efba9-132">Добавление определения для нового пользовательского поля</span><span class="sxs-lookup"><span data-stu-id="efba9-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="efba9-133">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="efba9-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="efba9-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="efba9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="efba9-135">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="efba9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="efba9-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="efba9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="efba9-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="efba9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

