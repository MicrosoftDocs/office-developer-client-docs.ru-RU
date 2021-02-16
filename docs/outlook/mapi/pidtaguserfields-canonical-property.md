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
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360741"
---
# <a name="pidtaguserfields-canonical-property"></a><span data-ttu-id="a8356-103">Каноническое свойство PidTagUserFields</span><span class="sxs-lookup"><span data-stu-id="a8356-103">PidTagUserFields Canonical Property</span></span>

  
  
<span data-ttu-id="a8356-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8356-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8356-105">Содержит имя, тип данных и другие сведения о пользовательском поле.</span><span class="sxs-lookup"><span data-stu-id="a8356-105">Contains the name, data type, and other information about a user-defined field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a8356-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a8356-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a8356-107">PR_USERFIELDS</span><span class="sxs-lookup"><span data-stu-id="a8356-107">PR_USERFIELDS</span></span>  <br/> |
|<span data-ttu-id="a8356-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a8356-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a8356-109">0x36E3</span><span class="sxs-lookup"><span data-stu-id="a8356-109">0x36E3</span></span>  <br/> |
|<span data-ttu-id="a8356-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a8356-110">Data type:</span></span>  <br/> |<span data-ttu-id="a8356-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a8356-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a8356-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a8356-112">Area:</span></span>  <br/> |<span data-ttu-id="a8356-113">Папка MAPI</span><span class="sxs-lookup"><span data-stu-id="a8356-113">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8356-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8356-114">Remarks</span></span>

<span data-ttu-id="a8356-115">Для каждого элемента Outlook сохраняет определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего **объекта IMessage.**</span><span class="sxs-lookup"><span data-stu-id="a8356-115">For each item, Outlook stores the definitions of all user-defined fields in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property of the corresponding **IMessage** object.</span></span> <span data-ttu-id="a8356-116">Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известный как [PropertyDefinition,](propertydefinition-stream-structure.md)который содержит определения полей.</span><span class="sxs-lookup"><span data-stu-id="a8356-116">The **PidLidPropertyDefinitionStream** property contains a binary stream known as [PropertyDefinition](propertydefinition-stream-structure.md), which contains the field definitions.</span></span> <span data-ttu-id="a8356-117">Дополнительные сведения о структурах потоков для определений полей см. в [подстройки Stream.](stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="a8356-117">For more information about stream structures for field definitions, see [Stream Structures](stream-structures.md).</span></span>
  
<span data-ttu-id="a8356-118">Для каждой папки Outlook сохраняет определения всех пользовательских полей в этой папке в свойстве **PidTagUserFields** связанного сообщения класса IPC.MS. REN. USERFIELDS — каждая папка, которая, как предполагается, содержит не более одного сообщения этого класса в связанной с ней таблицей содержимого.</span><span class="sxs-lookup"><span data-stu-id="a8356-118">For each folder, Outlook stores the definitions of all user-defined fields in that folder in the **PidTagUserFields** property of an associated message of the message class IPC.MS.REN.USERFIELDS - each folder presumed to contain no more than one message of this class in its associated contents table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a8356-119">Набор пользовательских полей в папке может не обязательно совпадать с наборами пользовательских полей в каждом из элементов.</span><span class="sxs-lookup"><span data-stu-id="a8356-119">The set of user-defined fields in a folder may not necessarily match the sets of user-defined fields in each of its items.</span></span> 
  
<span data-ttu-id="a8356-120">Набор пользовательских полей в папке отображается в различных местах пользовательского интерфейса Outlook, таких как выбор полей папки.</span><span class="sxs-lookup"><span data-stu-id="a8356-120">The set of user-defined fields in a folder is displayed in various places in the Outlook UI, such as the folder's Field Chooser.</span></span> <span data-ttu-id="a8356-121">Свойство **PidTagUserFields** сообщения содержит двоичный поток **FolderUserFields,** который содержит определения полей папки.</span><span class="sxs-lookup"><span data-stu-id="a8356-121">The message's **PidTagUserFields** property contains a binary stream, **FolderUserFields**, which contains the folder field definitions.</span></span> <span data-ttu-id="a8356-122">Дополнительные сведения о структурах потоков для определений полей папок см. в примере структуры потока полей папок и пример потока [FolderUserFields.](folderuserfields-stream-sample.md) [](folder-fields-stream-structures.md)</span><span class="sxs-lookup"><span data-stu-id="a8356-122">For more information about stream structures for folder field definitions, see [Folder Fields Stream Structures](folder-fields-stream-structures.md) and the [FolderUserFields Stream Sample](folderuserfields-stream-sample.md).</span></span>
  
## <a name="section-heading"></a><span data-ttu-id="a8356-123">Заголовок раздела</span><span class="sxs-lookup"><span data-stu-id="a8356-123">Section Heading</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a8356-124">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a8356-124">Protocol specifications</span></span>

<span data-ttu-id="a8356-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a8356-125">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a8356-126">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="a8356-126">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a8356-127">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a8356-127">Header files</span></span>

<span data-ttu-id="a8356-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a8356-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="a8356-129">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a8356-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a8356-130">См. также</span><span class="sxs-lookup"><span data-stu-id="a8356-130">See also</span></span>



[<span data-ttu-id="a8356-131">Элементы и поля Outlook</span><span class="sxs-lookup"><span data-stu-id="a8356-131">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="a8356-132">Добавление определения для нового поля User-Defined</span><span class="sxs-lookup"><span data-stu-id="a8356-132">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="a8356-133">Пример потока PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8356-133">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)
  
[<span data-ttu-id="a8356-134">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a8356-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a8356-135">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a8356-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a8356-136">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a8356-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a8356-137">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a8356-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

