---
title: Каноническое свойство PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383060"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="91df7-103">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="91df7-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="91df7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91df7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91df7-105">Содержит значение TRUE, если свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) имеет то же содержимое текста как свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="91df7-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91df7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="91df7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91df7-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="91df7-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="91df7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="91df7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91df7-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="91df7-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="91df7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="91df7-110">Data type:</span></span>  <br/> |<span data-ttu-id="91df7-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="91df7-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="91df7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="91df7-112">Area:</span></span>  <br/> |<span data-ttu-id="91df7-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="91df7-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91df7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="91df7-114">Remarks</span></span>

<span data-ttu-id="91df7-115">Значение TRUE означает, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), версия обычного текста сообщения и свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) версии форматированный текст (RTF), идентичны за исключением пробелы в **PR_BODY** и форматирование в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="91df7-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="91df7-116">Текст в двух версий состоит из те же символы в той последовательности.</span><span class="sxs-lookup"><span data-stu-id="91df7-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="91df7-117">Значение FALSE, означает, что две версии не синхронизированы для текстового контента, но позволяют выполнять синхронизацию с помощью функции [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="91df7-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="91df7-118">Изменил одной версии и не имеет другой версии.</span><span class="sxs-lookup"><span data-stu-id="91df7-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="91df7-119">Значение не означает, что две версии, если оба существует, или когда-либо существовало не удалось выполнить синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="91df7-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="91df7-120">Одной версии был удален или изменен радикально, что синхронизация невозможна.</span><span class="sxs-lookup"><span data-stu-id="91df7-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="91df7-121">Клиентское приложение, которое были изменены **PR_RTF_COMPRESSED** необходимо задать значение FALSE в этом свойстве для принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91df7-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="91df7-122">Хранилищ принять во внимание RTF сообщений следует выполнять синхронизацию с помощью **RTFSync** во время вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="91df7-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="91df7-123">Принять во внимание RTF клиентов следует проверить значение **PR_RTF_IN_SYNC** перед чтением **PR_RTF_COMPRESSED**и сначала вызывать **RTFSync** , если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="91df7-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="91df7-124">Если **PR_BODY** у которого изменения отличное от его пробелы, хранилище сообщений необходимо удалить **PR_RTF_IN_SYNC** для завершения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="91df7-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="91df7-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="91df7-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="91df7-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="91df7-126">Protocol specifications</span></span>

<span data-ttu-id="91df7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91df7-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91df7-128">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="91df7-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="91df7-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="91df7-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="91df7-130">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="91df7-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="91df7-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="91df7-131">Header files</span></span>

<span data-ttu-id="91df7-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91df7-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="91df7-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="91df7-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="91df7-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="91df7-134">Mapitags.h</span></span>
  
> <span data-ttu-id="91df7-135">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="91df7-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91df7-136">См. также</span><span class="sxs-lookup"><span data-stu-id="91df7-136">See also</span></span>



[<span data-ttu-id="91df7-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91df7-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91df7-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="91df7-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91df7-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="91df7-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91df7-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="91df7-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

