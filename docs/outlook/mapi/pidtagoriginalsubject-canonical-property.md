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
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331145"
---
# <a name="pidtagoriginalsubject-canonical-property"></a><span data-ttu-id="0386c-103">Каноническое свойство PidTagOriginalSubject</span><span class="sxs-lookup"><span data-stu-id="0386c-103">PidTagOriginalSubject Canonical Property</span></span>

  
  
<span data-ttu-id="0386c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0386c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0386c-105">Содержит тему исходного сообщения для использования в отчете о сообщении.</span><span class="sxs-lookup"><span data-stu-id="0386c-105">Contains the subject of an original message for use in a report about the message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0386c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0386c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0386c-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="0386c-107">PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="0386c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0386c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0386c-109">0x0049</span><span class="sxs-lookup"><span data-stu-id="0386c-109">0x0049</span></span>  <br/> |
|<span data-ttu-id="0386c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0386c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0386c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0386c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0386c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0386c-112">Area:</span></span>  <br/> |<span data-ttu-id="0386c-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="0386c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0386c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0386c-114">Remarks</span></span>

<span data-ttu-id="0386c-115">Изначально для этих свойств задавалось то же **значение, что** и для свойства PR_SUBJECT ([PidTagSubject).](pidtagsubject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0386c-115">These properties are originally set to the same value as the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="0386c-116">Свойства темы, как правило, являются небольшими строками менее 256 символов, и поставщик хранилище сообщений не обязан поддерживать интерфейс **IStream** для связывания и встраиния объектов (OLE).</span><span class="sxs-lookup"><span data-stu-id="0386c-116">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="0386c-117">Клиент всегда должен сначала попытаться получить доступ через интерфейс **IMAPIProp** и использовать **IStream** только **MAPI_E_NOT_ENOUGH_MEMORY** возвращается.</span><span class="sxs-lookup"><span data-stu-id="0386c-117">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0386c-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0386c-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0386c-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="0386c-119">Protocol specifications</span></span>

<span data-ttu-id="0386c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0386c-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0386c-121">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="0386c-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0386c-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0386c-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0386c-123">Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.</span><span class="sxs-lookup"><span data-stu-id="0386c-123">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="0386c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0386c-124">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0386c-125">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="0386c-125">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0386c-126">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="0386c-126">Header files</span></span>

<span data-ttu-id="0386c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0386c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0386c-128">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0386c-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0386c-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0386c-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0386c-130">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0386c-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0386c-131">См. также</span><span class="sxs-lookup"><span data-stu-id="0386c-131">See also</span></span>



[<span data-ttu-id="0386c-132">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0386c-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0386c-133">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0386c-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0386c-134">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0386c-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0386c-135">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="0386c-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

