---
title: Каноническое свойство PidTagReadReceiptRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReadReceiptRequested
api_type:
- COM
ms.assetid: 7db0645b-f3ab-4fc4-b865-68c952aeb359
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1d4d4404d175458d5b708948b11c93b734a8bd1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811619"
---
# <a name="pidtagreadreceiptrequested-canonical-property"></a><span data-ttu-id="01667-103">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="01667-103">PidTagReadReceiptRequested Canonical Property</span></span>

  
  
<span data-ttu-id="01667-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01667-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01667-105">Содержит значение TRUE, если отправитель сообщения запрашивает системы обмена сообщениями для создания чтения отчета, когда получатель сообщения.</span><span class="sxs-lookup"><span data-stu-id="01667-105">Contains TRUE if a message sender wants the messaging system to generate a read report when the recipient has read a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="01667-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="01667-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="01667-107">PR_READ_RECEIPT_REQUESTED</span><span class="sxs-lookup"><span data-stu-id="01667-107">PR_READ_RECEIPT_REQUESTED</span></span>  <br/> |
|<span data-ttu-id="01667-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="01667-108">Identifier:</span></span>  <br/> |<span data-ttu-id="01667-109">0x0029</span><span class="sxs-lookup"><span data-stu-id="01667-109">0x0029</span></span>  <br/> |
|<span data-ttu-id="01667-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="01667-110">Data type:</span></span>  <br/> |<span data-ttu-id="01667-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="01667-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="01667-112">Область:</span><span class="sxs-lookup"><span data-stu-id="01667-112">Area:</span></span>  <br/> |<span data-ttu-id="01667-113">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="01667-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01667-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="01667-114">Remarks</span></span>

<span data-ttu-id="01667-115">Это свойство должно быть присвоено значение TRUE для проверки значения свойства **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) и **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="01667-115">This property must be set to TRUE to validate the values in the **PR_READ_RECEIPT_ENTRYID** ([PidTagReadReceiptEntryId](pidtagreadreceiptentryid-canonical-property.md)) and **PR_READ_RECEIPT_SEARCH_KEY** ([PidTagReadReceiptSearchKey](pidtagreadreceiptsearchkey-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="01667-116">Если сообщение с набором **PR_READ_RECEIPT_REQUESTED** удаляется или истекает до системы обмена сообщениями можно создать отчет о чтения, nonread отчет создается.</span><span class="sxs-lookup"><span data-stu-id="01667-116">If a message with **PR_READ_RECEIPT_REQUESTED** set is deleted or expires before the messaging system can generate a read report, a nonread report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="01667-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="01667-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="01667-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="01667-118">Protocol specifications</span></span>

<span data-ttu-id="01667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01667-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01667-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="01667-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="01667-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="01667-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="01667-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="01667-122">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="01667-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="01667-123">Header files</span></span>

<span data-ttu-id="01667-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01667-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="01667-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="01667-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="01667-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="01667-126">Mapitags.h</span></span>
  
> <span data-ttu-id="01667-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="01667-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01667-128">См. также</span><span class="sxs-lookup"><span data-stu-id="01667-128">See also</span></span>



[<span data-ttu-id="01667-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01667-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="01667-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="01667-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="01667-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="01667-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="01667-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="01667-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

