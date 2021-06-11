---
title: Каноническое свойство PidLidContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContacts
api_type:
- COM
ms.assetid: 709e701f-b24e-4cd5-8c55-3f9e67f67a4a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 10dd12522a635098908285f1a9ee16c93d96f728
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319462"
---
# <a name="pidlidcontacts-canonical-property"></a><span data-ttu-id="6a930-103">Каноническое свойство PidLidContacts</span><span class="sxs-lookup"><span data-stu-id="6a930-103">PidLidContacts Canonical Property</span></span>

  
  
<span data-ttu-id="6a930-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a930-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a930-105">Содержит имена контактов, связанных с элементом.</span><span class="sxs-lookup"><span data-stu-id="6a930-105">Contains the names of contacts associated with the item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a930-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6a930-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6a930-107">dispidContacts</span><span class="sxs-lookup"><span data-stu-id="6a930-107">dispidContacts</span></span>  <br/> |
|<span data-ttu-id="6a930-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="6a930-108">Property set:</span></span>  <br/> |<span data-ttu-id="6a930-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="6a930-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="6a930-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="6a930-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="6a930-111">0x0000853A</span><span class="sxs-lookup"><span data-stu-id="6a930-111">0x0000853A</span></span>  <br/> |
|<span data-ttu-id="6a930-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6a930-112">Data type:</span></span>  <br/> |<span data-ttu-id="6a930-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6a930-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6a930-114">Область:</span><span class="sxs-lookup"><span data-stu-id="6a930-114">Area:</span></span>  <br/> |<span data-ttu-id="6a930-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="6a930-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a930-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a930-116">Remarks</span></span>

<span data-ttu-id="6a930-117">Это свойство содержит **свойство PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)каждого  входа в адресную книгу, ссылаясь на значение **dispidContactLinkEntry** [(свойство PidLidContactLinkEntry).](pidlidcontactlinkentry-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6a930-117">This property contains the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of each Address Book **EntryID** that is referenced in the value of **dispidContactLinkEntry** ([PidLidContactLinkEntry](pidlidcontactlinkentry-canonical-property.md)) property.</span></span> <span data-ttu-id="6a930-118">Он может включать имена, не ссылаясь на **dispidContactLinkEntry**.</span><span class="sxs-lookup"><span data-stu-id="6a930-118">It may include names not referenced in **dispidContactLinkEntry**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6a930-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6a930-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6a930-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6a930-120">Protocol specifications</span></span>

<span data-ttu-id="6a930-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a930-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a930-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6a930-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6a930-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a930-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a930-124">Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6a930-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="6a930-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a930-125">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a930-126">Указывает свойства и операции, которые допустимы для журналов.</span><span class="sxs-lookup"><span data-stu-id="6a930-126">Specifies the properties and operations that are permissible for journals.</span></span>
    
<span data-ttu-id="6a930-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6a930-127">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6a930-128">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="6a930-128">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6a930-129">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6a930-129">Header files</span></span>

<span data-ttu-id="6a930-130">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6a930-130">Mapidefs.h</span></span>
  
> <span data-ttu-id="6a930-131">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6a930-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a930-132">См. также</span><span class="sxs-lookup"><span data-stu-id="6a930-132">See also</span></span>



[<span data-ttu-id="6a930-133">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a930-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6a930-134">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6a930-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6a930-135">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6a930-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6a930-136">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6a930-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

