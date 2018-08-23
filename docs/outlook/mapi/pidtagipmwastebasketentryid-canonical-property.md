---
title: Каноническое свойство PidTagIpmWastebasketEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmWastebasketEntryId
api_type:
- HeaderDef
ms.assetid: 0f8dd043-66f0-4193-9b95-853bc3827f73
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 66bbf49d737c42ecc2f6c765a60540163649f447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573896"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="08743-103">Каноническое свойство PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="08743-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="08743-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08743-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08743-105">Содержит идентификатор записи из папки "Удаленные" standard электронной почты — это сообщение (IPM).</span><span class="sxs-lookup"><span data-stu-id="08743-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08743-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="08743-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08743-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="08743-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="08743-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="08743-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08743-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="08743-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="08743-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="08743-110">Data type:</span></span>  <br/> |<span data-ttu-id="08743-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="08743-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="08743-112">Область:</span><span class="sxs-lookup"><span data-stu-id="08743-112">Area:</span></span>  <br/> |<span data-ttu-id="08743-113">Folder</span><span class="sxs-lookup"><span data-stu-id="08743-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08743-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="08743-114">Remarks</span></span>

<span data-ttu-id="08743-115">Клиентское приложение следует переместить удаленных сообщений электронной почты — это папки "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="08743-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="08743-116">Если сообщение уже присутствует в этой папке, если это свойство не поддерживается, удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="08743-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08743-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="08743-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="08743-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="08743-118">Header files</span></span>

<span data-ttu-id="08743-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08743-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="08743-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="08743-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="08743-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="08743-121">Mapitags.h</span></span>
  
> <span data-ttu-id="08743-122">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="08743-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08743-123">См. также</span><span class="sxs-lookup"><span data-stu-id="08743-123">See also</span></span>



[<span data-ttu-id="08743-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08743-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08743-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="08743-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08743-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="08743-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08743-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="08743-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

