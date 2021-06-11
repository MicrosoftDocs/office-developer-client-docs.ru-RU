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
# <a name="pidtagrtfinsync-canonical-property"></a><span data-ttu-id="f8b16-103">Каноническое свойство PidTagRtfInSync</span><span class="sxs-lookup"><span data-stu-id="f8b16-103">PidTagRtfInSync Canonical Property</span></span>

  
  
<span data-ttu-id="f8b16-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8b16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8b16-105">Содержит **TRUE, если свойство PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)имеет такое же текстовое **содержимое,** как и свойство PR_BODY [(PidTagBody)](pidtagbody-canonical-property.md)для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="f8b16-105">Contains TRUE if the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property has the same text content as the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f8b16-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f8b16-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f8b16-107">PR_RTF_IN_SYNC</span><span class="sxs-lookup"><span data-stu-id="f8b16-107">PR_RTF_IN_SYNC</span></span>  <br/> |
|<span data-ttu-id="f8b16-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f8b16-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f8b16-109">0x0E1F</span><span class="sxs-lookup"><span data-stu-id="f8b16-109">0x0E1F</span></span>  <br/> |
|<span data-ttu-id="f8b16-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f8b16-110">Data type:</span></span>  <br/> |<span data-ttu-id="f8b16-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f8b16-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f8b16-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f8b16-112">Area:</span></span>  <br/> |<span data-ttu-id="f8b16-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="f8b16-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8b16-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f8b16-114">Remarks</span></span>

<span data-ttu-id="f8b16-115">Значение TRUE означает, что **свойство PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md)обычная текстовая версия этого сообщения и **свойство PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)версии Rich Text Format (RTF) идентичны, за исключением белого пространства в **PR_BODY** и форматирования **в PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="f8b16-115">A value of TRUE means that the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property, the plain text version of this message, and the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property, the Rich Text Format (RTF) version, are identical except for white space in **PR_BODY** and formatting in **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="f8b16-116">Текст в двух версиях состоит из одного и того же символа в одной последовательности.</span><span class="sxs-lookup"><span data-stu-id="f8b16-116">The text in the two versions consists of the same characters in the same sequence.</span></span>
  
<span data-ttu-id="f8b16-117">Значение FALSE означает, что две версии не синхронизируются для текстового контента, но могут быть синхронизированы функцией [RTFSync.](rtfsync.md)</span><span class="sxs-lookup"><span data-stu-id="f8b16-117">A value of FALSE means that the two versions are not synchronized for text content but are capable of being synchronized by the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="f8b16-118">Одна версия была изменена, а другая нет.</span><span class="sxs-lookup"><span data-stu-id="f8b16-118">One version has been altered and the other version has not.</span></span> 
  
<span data-ttu-id="f8b16-119">Отсутствие значения означает, что две версии, если они существуют или когда-либо существовали, не могут быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="f8b16-119">No value means that the two versions, if both exist or ever existed, cannot be synchronized.</span></span> <span data-ttu-id="f8b16-120">Одна из версий была удалена или изменена настолько радикально, что синхронизация больше не возможна.</span><span class="sxs-lookup"><span data-stu-id="f8b16-120">One version has been deleted or altered so radically that synchronization is no longer possible.</span></span>
  
<span data-ttu-id="f8b16-121">Клиентский приложение, которое **PR_RTF_COMPRESSED,** должно установить значение FALSE в этом свойстве для принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f8b16-121">A client application that has modified **PR_RTF_COMPRESSED** should set a value of FALSE in this property to force synchronization.</span></span> <span data-ttu-id="f8b16-122">RTF-хранилища сообщений должны выполнять синхронизацию с помощью **RTFSync** во время вызова [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="f8b16-122">RTF-aware message stores should perform the synchronization using **RTFSync** during an [IMAPIProp::SaveChanges](imapiprop-savechanges.md) call.</span></span> <span data-ttu-id="f8b16-123">Клиенты, осведомленные о RTF, должны проверить параметр PR_RTF_IN_SYNC перед чтением PR_RTF_COMPRESSED **и** при необходимости вызвать **RTFSync.** </span><span class="sxs-lookup"><span data-stu-id="f8b16-123">RTF-aware clients should check the setting of **PR_RTF_IN_SYNC** before reading **PR_RTF_COMPRESSED**, and call **RTFSync** first if necessary.</span></span> 
  
<span data-ttu-id="f8b16-124">Если **PR_BODY** был внесены изменения в что-либо, кроме белого  пространства, хранилище сообщений должно удалить PR_RTF_IN_SYNC, чтобы завершить синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="f8b16-124">If **PR_BODY** has had modifications to anything other than its white space, the message store must delete **PR_RTF_IN_SYNC** to terminate synchronization.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f8b16-125">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f8b16-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f8b16-126">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f8b16-126">Protocol specifications</span></span>

<span data-ttu-id="f8b16-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8b16-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8b16-128">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f8b16-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f8b16-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f8b16-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f8b16-130">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="f8b16-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f8b16-131">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f8b16-131">Header files</span></span>

<span data-ttu-id="f8b16-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f8b16-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="f8b16-133">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f8b16-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="f8b16-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f8b16-134">Mapitags.h</span></span>
  
> <span data-ttu-id="f8b16-135">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f8b16-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f8b16-136">См. также</span><span class="sxs-lookup"><span data-stu-id="f8b16-136">See also</span></span>



[<span data-ttu-id="f8b16-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b16-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f8b16-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b16-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f8b16-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f8b16-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f8b16-140">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f8b16-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

