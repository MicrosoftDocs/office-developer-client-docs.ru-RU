---
title: Каноническое свойство PidTagReadReceiptEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptEntryId
api_type:
- COM
ms.assetid: 141d49c8-87cf-4d80-a33b-ccbf3eeae19e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 82bc5fd99df115527f703eff7261d02d1bf4d3ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811611"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="8a46c-103">Каноническое свойство PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="8a46c-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8a46c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a46c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a46c-105">Содержит идентификатор записи для обмена сообщениями пользователя, где системы обмена сообщениями необходимо прямое подключение чтения отчет для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a46c-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a46c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8a46c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8a46c-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8a46c-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8a46c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="8a46c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8a46c-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="8a46c-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="8a46c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8a46c-110">Data type:</span></span>  <br/> |<span data-ttu-id="8a46c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8a46c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8a46c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="8a46c-112">Area:</span></span>  <br/> |<span data-ttu-id="8a46c-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="8a46c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a46c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a46c-114">Remarks</span></span>

<span data-ttu-id="8a46c-115">Это свойство игнорируется, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) не установлен в значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="8a46c-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="8a46c-116">Если клиентское приложение может принимать чтение отчетов, его можно оставить это свойство неопределенные или задайте для него значение идентификатор записи, содержащиеся в свойстве **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a46c-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8a46c-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8a46c-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8a46c-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8a46c-118">Protocol specifications</span></span>

<span data-ttu-id="8a46c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a46c-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a46c-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8a46c-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8a46c-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8a46c-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8a46c-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8a46c-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8a46c-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="8a46c-123">Header files</span></span>

<span data-ttu-id="8a46c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a46c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8a46c-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8a46c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8a46c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8a46c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8a46c-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="8a46c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8a46c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8a46c-128">See also</span></span>



[<span data-ttu-id="8a46c-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a46c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8a46c-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8a46c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8a46c-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8a46c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8a46c-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8a46c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

