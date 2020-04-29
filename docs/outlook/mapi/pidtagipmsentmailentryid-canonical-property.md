---
title: Каноническое свойство PidTagIpmSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSentMailEntryId
api_type:
- HeaderDef
ms.assetid: f6877435-6b26-4060-924f-a65591ad9538
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fd29afc93bc952bb619dfac752fae232bf7991cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437324"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="cc5e3-103">Каноническое свойство PidTagIpmSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="cc5e3-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="cc5e3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc5e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc5e3-105">Содержит идентификатор стандартной папки "Отправленные" сообщений об ошибках (IPM).</span><span class="sxs-lookup"><span data-stu-id="cc5e3-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc5e3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="cc5e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cc5e3-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cc5e3-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="cc5e3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="cc5e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cc5e3-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="cc5e3-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="cc5e3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="cc5e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="cc5e3-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cc5e3-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cc5e3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="cc5e3-112">Area:</span></span>  <br/> |<span data-ttu-id="cc5e3-113">Folder</span><span class="sxs-lookup"><span data-stu-id="cc5e3-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc5e3-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc5e3-114">Remarks</span></span>

<span data-ttu-id="cc5e3-115">После отправки межпользовательские сообщения обычно помещаются в папку "Отправленные".</span><span class="sxs-lookup"><span data-stu-id="cc5e3-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="cc5e3-116">Клиент может использовать это свойство, чтобы задать свойство **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) для отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cc5e3-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="cc5e3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="cc5e3-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="cc5e3-118">Header files</span></span>

<span data-ttu-id="cc5e3-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="cc5e3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="cc5e3-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="cc5e3-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="cc5e3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="cc5e3-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="cc5e3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cc5e3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="cc5e3-123">See also</span></span>



[<span data-ttu-id="cc5e3-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="cc5e3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cc5e3-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="cc5e3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cc5e3-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="cc5e3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cc5e3-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="cc5e3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

