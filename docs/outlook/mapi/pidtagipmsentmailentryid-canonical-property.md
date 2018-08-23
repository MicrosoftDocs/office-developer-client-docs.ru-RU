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
ms.openlocfilehash: ee2e9e7f73e03e0a201a5ff41ea6e37a78c668a1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569577"
---
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="02e57-103">Каноническое свойство PidTagIpmSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="02e57-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="02e57-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02e57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02e57-105">Содержит идентификатор записи папки Отправленные стандартные сообщения электронной почты — это (IPM).</span><span class="sxs-lookup"><span data-stu-id="02e57-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02e57-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="02e57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02e57-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="02e57-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="02e57-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="02e57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02e57-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="02e57-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="02e57-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="02e57-110">Data type:</span></span>  <br/> |<span data-ttu-id="02e57-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="02e57-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="02e57-112">Область:</span><span class="sxs-lookup"><span data-stu-id="02e57-112">Area:</span></span>  <br/> |<span data-ttu-id="02e57-113">Folder</span><span class="sxs-lookup"><span data-stu-id="02e57-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02e57-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="02e57-114">Remarks</span></span>

<span data-ttu-id="02e57-115">После отправки, сообщения электронной почты — это обычно размещается в папке «Отправленные».</span><span class="sxs-lookup"><span data-stu-id="02e57-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="02e57-116">Клиент может использовать это свойство для свойства **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) на отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="02e57-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02e57-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="02e57-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="02e57-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="02e57-118">Header files</span></span>

<span data-ttu-id="02e57-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02e57-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="02e57-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="02e57-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="02e57-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02e57-121">Mapitags.h</span></span>
  
> <span data-ttu-id="02e57-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="02e57-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02e57-123">См. также</span><span class="sxs-lookup"><span data-stu-id="02e57-123">See also</span></span>



[<span data-ttu-id="02e57-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02e57-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02e57-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="02e57-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02e57-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="02e57-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02e57-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="02e57-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

