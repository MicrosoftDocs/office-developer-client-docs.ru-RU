---
title: Каноническое свойство PidTagReadReceiptSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptSearchKey
api_type:
- COM
ms.assetid: a0ea5628-1393-4ab8-bc34-a58cf130db51
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7016b1a7039d5df8d4e9fdedea580526eebe04bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585943"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="bae3d-103">Каноническое свойство PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="bae3d-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="bae3d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bae3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bae3d-105">Содержит ключ поиска для обмена сообщениями пользователя, к которому система обмена сообщениями направляет просмотра отчетов для сообщения.</span><span class="sxs-lookup"><span data-stu-id="bae3d-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bae3d-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bae3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bae3d-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bae3d-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="bae3d-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bae3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bae3d-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="bae3d-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="bae3d-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bae3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="bae3d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bae3d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bae3d-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bae3d-112">Area:</span></span>  <br/> |<span data-ttu-id="bae3d-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="bae3d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bae3d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bae3d-114">Remarks</span></span>

<span data-ttu-id="bae3d-115">Это свойство игнорируется, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) не установлен в значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="bae3d-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="bae3d-116">Если клиентское приложение может принимать чтение отчетов, его можно оставить это свойство неопределенные или задайте для него значение ключа поиска, содержащихся в свойстве **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="bae3d-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bae3d-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bae3d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bae3d-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bae3d-118">Protocol specifications</span></span>

<span data-ttu-id="bae3d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae3d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae3d-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bae3d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bae3d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bae3d-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bae3d-122">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="bae3d-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bae3d-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bae3d-123">Header files</span></span>

<span data-ttu-id="bae3d-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="bae3d-124">Mapidef.h</span></span>
  
> <span data-ttu-id="bae3d-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bae3d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="bae3d-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bae3d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="bae3d-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bae3d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bae3d-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bae3d-128">See also</span></span>



[<span data-ttu-id="bae3d-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bae3d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bae3d-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bae3d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bae3d-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bae3d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bae3d-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bae3d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

