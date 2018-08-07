---
title: Каноническое свойство PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6cf81a5b4c10cb7bff5f03a1b25d11bbaa8ff277
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811479"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="638ff-103">Каноническое свойство PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="638ff-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="638ff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="638ff-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="638ff-105">Содержит темы исходного сообщения для использования в отчете о сообщении.</span><span class="sxs-lookup"><span data-stu-id="638ff-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="638ff-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="638ff-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="638ff-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="638ff-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="638ff-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="638ff-108">Identifier:</span></span>  <br/> |<span data-ttu-id="638ff-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="638ff-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="638ff-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="638ff-110">Data type:</span></span>  <br/> |<span data-ttu-id="638ff-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="638ff-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="638ff-112">Область:</span><span class="sxs-lookup"><span data-stu-id="638ff-112">Area:</span></span>  <br/> |<span data-ttu-id="638ff-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="638ff-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="638ff-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="638ff-114">Remarks</span></span>

<span data-ttu-id="638ff-115">Эти свойства изначально устанавливаются совпадает со значением свойства **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="638ff-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="638ff-116">Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддерживают интерфейс объекта связывания и внедрения (OLE) **IStream** на них.</span><span class="sxs-lookup"><span data-stu-id="638ff-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="638ff-117">Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается **MAPI_E_NOT_ENOUGH_MEMORY** .</span><span class="sxs-lookup"><span data-stu-id="638ff-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="638ff-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="638ff-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="638ff-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="638ff-119">Protocol specifications</span></span>

<span data-ttu-id="638ff-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="638ff-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="638ff-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="638ff-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="638ff-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="638ff-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="638ff-123">Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="638ff-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="638ff-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="638ff-124">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="638ff-125">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="638ff-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="638ff-126">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="638ff-126">Header files</span></span>

<span data-ttu-id="638ff-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="638ff-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="638ff-128">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="638ff-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="638ff-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="638ff-129">Mapitags.h</span></span>
  
> <span data-ttu-id="638ff-130">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="638ff-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="638ff-131">См. также</span><span class="sxs-lookup"><span data-stu-id="638ff-131">See also</span></span>



[<span data-ttu-id="638ff-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="638ff-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="638ff-133">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="638ff-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="638ff-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="638ff-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="638ff-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="638ff-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

