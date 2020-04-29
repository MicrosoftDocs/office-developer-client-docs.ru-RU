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
ms.openlocfilehash: 3794386c4461c90f973e4028132cb8220dfaa19b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426354"
---
# <a name="pidtagipmwastebasketentryid-canonical-property"></a><span data-ttu-id="2c499-103">Каноническое свойство PidTagIpmWastebasketEntryId</span><span class="sxs-lookup"><span data-stu-id="2c499-103">PidTagIpmWastebasketEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="2c499-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c499-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c499-105">Содержит идентификатор стандартной папки "Удаленные" межпользовательского сообщения (IPM).</span><span class="sxs-lookup"><span data-stu-id="2c499-105">Contains the entry identifier of the standard interpersonal message (IPM) Deleted Items folder.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c499-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2c499-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c499-107">PR_IPM_WASTEBASKET_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2c499-107">PR_IPM_WASTEBASKET_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="2c499-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2c499-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c499-109">0x35E3</span><span class="sxs-lookup"><span data-stu-id="2c499-109">0x35E3</span></span>  <br/> |
|<span data-ttu-id="2c499-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2c499-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c499-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="2c499-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="2c499-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2c499-112">Area:</span></span>  <br/> |<span data-ttu-id="2c499-113">Folder</span><span class="sxs-lookup"><span data-stu-id="2c499-113">Folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c499-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c499-114">Remarks</span></span>

<span data-ttu-id="2c499-115">Клиентское приложение должно перемещать удаленные межпользовательские сообщения в папку "Удаленные".</span><span class="sxs-lookup"><span data-stu-id="2c499-115">A client application should move deleted interpersonal messages to the Deleted Items folder.</span></span> <span data-ttu-id="2c499-116">Если сообщение уже находится в этой папке или если это свойство не поддерживается, клиент должен удалить сообщение.</span><span class="sxs-lookup"><span data-stu-id="2c499-116">If the message is already in this folder, or if this property is not supported, the client should delete the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2c499-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2c499-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2c499-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2c499-118">Header files</span></span>

<span data-ttu-id="2c499-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2c499-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c499-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2c499-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c499-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="2c499-121">Mapitags.h</span></span>
  
> <span data-ttu-id="2c499-122">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="2c499-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c499-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2c499-123">See also</span></span>



[<span data-ttu-id="2c499-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2c499-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c499-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="2c499-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c499-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2c499-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c499-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2c499-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

