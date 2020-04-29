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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357878"
---
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="9ef97-103">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="9ef97-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="9ef97-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ef97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ef97-105">Содержит значение TRUE, если свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) имеет то же текстовое содержимое, что и свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ef97-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ef97-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="9ef97-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ef97-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="9ef97-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="9ef97-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="9ef97-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ef97-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="9ef97-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="9ef97-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9ef97-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ef97-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9ef97-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9ef97-112">Область:</span><span class="sxs-lookup"><span data-stu-id="9ef97-112">Area:</span></span>  <br/> |<span data-ttu-id="9ef97-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="9ef97-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ef97-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9ef97-114">Remarks</span></span>

<span data-ttu-id="9ef97-115">Значение TRUE означает, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), версия обычного текста этого сообщения и свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), версия RTF, идентичны за исключением пробелов в **PR_BODY** и форматирования в **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="9ef97-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="9ef97-116">Текст в двух версиях состоит из одних и тех же символов в одной и той же последовательности.</span><span class="sxs-lookup"><span data-stu-id="9ef97-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="9ef97-117">Значение FALSE означает, что две версии не синхронизируются для текстового содержимого, но могут быть синхронизированы с помощью функции [ртфсинк](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef97-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="9ef97-118">Одна и та же версия была изменена, а другая нет.</span><span class="sxs-lookup"><span data-stu-id="9ef97-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="9ef97-119">Значение не означает, что две версии (если они существуют или когда-либо существовали) не могут быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="9ef97-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="9ef97-120">Одна версия была удалена или изменена таким образом, что синхронизация более невозможна.</span><span class="sxs-lookup"><span data-stu-id="9ef97-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="9ef97-121">В клиентском приложении с измененными **PR_RTF_COMPRESSED** для принудительной синхронизации в этом свойстве должно быть задано значение false.</span><span class="sxs-lookup"><span data-stu-id="9ef97-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="9ef97-122">Хранилища сообщений с поддержкой RTF должны выполнять синхронизацию с помощью **ртфсинк** во время вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef97-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="9ef97-123">Клиенты, поддерживающие RTF, должны проверять параметры **PR_RTF_IN_SYNC** перед чтением **PR_RTF_COMPRESSED**, и при необходимости вызывать **ртфсинк** в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="9ef97-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="9ef97-124">Если **PR_BODY** имеет изменения, которые отличаются от пробелов, то хранилище сообщений должно удалить **PR_RTF_IN_SYNC** для завершения синхронизации.</span><span class="sxs-lookup"><span data-stu-id="9ef97-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ef97-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9ef97-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ef97-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9ef97-126">Protocol specifications</span></span>

<span data-ttu-id="9ef97-127">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ef97-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ef97-128">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9ef97-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ef97-129">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ef97-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ef97-130">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="9ef97-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ef97-131">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="9ef97-131">Header files</span></span>

<span data-ttu-id="9ef97-132">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9ef97-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ef97-133">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9ef97-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ef97-134">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="9ef97-134">Mapitags.h</span></span>
  
> <span data-ttu-id="9ef97-135">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="9ef97-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ef97-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9ef97-136">See also</span></span>



[<span data-ttu-id="9ef97-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef97-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ef97-138">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef97-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ef97-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef97-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ef97-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9ef97-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

