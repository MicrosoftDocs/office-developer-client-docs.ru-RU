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
# <a name="pidtagipmsentmailentryid-canonical-property"></a><span data-ttu-id="ee9af-103">Каноническое свойство PidTagIpmSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="ee9af-103">PidTagIpmSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="ee9af-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee9af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee9af-105">Содержит идентификатор записи стандартной папки отправленных элементов для межличностных сообщений (IPM).</span><span class="sxs-lookup"><span data-stu-id="ee9af-105">Contains the entry identifier of the standard interpersonal message (IPM) Sent Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee9af-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ee9af-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ee9af-107">PR_IPM_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ee9af-107">PR_IPM_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="ee9af-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ee9af-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ee9af-109">0x35E4</span><span class="sxs-lookup"><span data-stu-id="ee9af-109">0x35E4</span></span>  <br/> |
|<span data-ttu-id="ee9af-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ee9af-110">Data type:</span></span>  <br/> |<span data-ttu-id="ee9af-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ee9af-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ee9af-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ee9af-112">Area:</span></span>  <br/> |<span data-ttu-id="ee9af-113">Folder</span><span class="sxs-lookup"><span data-stu-id="ee9af-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee9af-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee9af-114">Remarks</span></span>

<span data-ttu-id="ee9af-115">После их отослания межличностные сообщения обычно помещаются в папку Отправленные элементы.</span><span class="sxs-lookup"><span data-stu-id="ee9af-115">After being sent, interpersonal messages are usually placed in the Sent Items folder.</span></span> <span data-ttu-id="ee9af-116">Клиент может использовать это свойство  для PR_SENTMAIL_ENTRYID[(PidTagSentMailEntryId)](pidtagsentmailentryid-canonical-property.md)в отправленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="ee9af-116">A client can use this property to set the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property on a submitted message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ee9af-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ee9af-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ee9af-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="ee9af-118">Header files</span></span>

<span data-ttu-id="ee9af-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ee9af-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ee9af-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ee9af-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ee9af-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ee9af-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ee9af-122">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="ee9af-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ee9af-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ee9af-123">See also</span></span>



[<span data-ttu-id="ee9af-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ee9af-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ee9af-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ee9af-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ee9af-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ee9af-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ee9af-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="ee9af-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

