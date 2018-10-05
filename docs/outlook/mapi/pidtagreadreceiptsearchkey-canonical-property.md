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
ms.openlocfilehash: aa92e224f10fd652078b965c8e3a0b5ab59cc388
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398733"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="a5040-103">Каноническое свойство PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="a5040-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a5040-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5040-105">Содержит ключ поиска для обмена сообщениями пользователя, к которому система обмена сообщениями направляет просмотра отчетов для сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5040-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5040-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5040-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5040-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a5040-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a5040-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a5040-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5040-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="a5040-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="a5040-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5040-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5040-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5040-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a5040-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a5040-112">Area:</span></span>  <br/> |<span data-ttu-id="a5040-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="a5040-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5040-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5040-114">Remarks</span></span>

<span data-ttu-id="a5040-115">Это свойство игнорируется, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) не установлен в значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a5040-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="a5040-116">Если клиентское приложение может принимать чтение отчетов, его можно оставить это свойство неопределенные или задайте для него значение ключа поиска, содержащихся в свойстве **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5040-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5040-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5040-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5040-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5040-118">Protocol specifications</span></span>

<span data-ttu-id="a5040-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5040-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5040-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5040-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5040-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5040-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5040-122">Задает свойства и операции, допустимые в сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a5040-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5040-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a5040-123">Header files</span></span>

<span data-ttu-id="a5040-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="a5040-124">Mapidef.h</span></span>
  
> <span data-ttu-id="a5040-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5040-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5040-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5040-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a5040-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a5040-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5040-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a5040-128">See also</span></span>



[<span data-ttu-id="a5040-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5040-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5040-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5040-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5040-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5040-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5040-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5040-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

