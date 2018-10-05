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
ms.openlocfilehash: 662c191f36f9ca30dcdf0f559ea5385bfe5fd305
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396437"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="d4f22-103">Каноническое свойство PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="d4f22-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="d4f22-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4f22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4f22-105">Содержит идентификатор записи для обмена сообщениями пользователя, где системы обмена сообщениями необходимо прямое подключение чтения отчет для данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="d4f22-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4f22-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d4f22-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4f22-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d4f22-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="d4f22-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d4f22-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d4f22-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="d4f22-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="d4f22-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d4f22-110">Data type:</span></span>  <br/> |<span data-ttu-id="d4f22-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d4f22-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d4f22-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d4f22-112">Area:</span></span>  <br/> |<span data-ttu-id="d4f22-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="d4f22-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4f22-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4f22-114">Remarks</span></span>

<span data-ttu-id="d4f22-115">Это свойство игнорируется, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) не установлен в значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="d4f22-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="d4f22-116">Если клиентское приложение может принимать чтение отчетов, его можно оставить это свойство неопределенные или задайте для него значение идентификатор записи, содержащиеся в свойстве **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="d4f22-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d4f22-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d4f22-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4f22-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d4f22-118">Protocol specifications</span></span>

<span data-ttu-id="d4f22-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4f22-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4f22-120">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d4f22-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4f22-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4f22-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4f22-122">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d4f22-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4f22-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d4f22-123">Header files</span></span>

<span data-ttu-id="d4f22-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4f22-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4f22-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d4f22-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="d4f22-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d4f22-126">Mapitags.h</span></span>
  
> <span data-ttu-id="d4f22-127">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d4f22-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4f22-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d4f22-128">See also</span></span>



[<span data-ttu-id="d4f22-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4f22-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4f22-130">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d4f22-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4f22-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d4f22-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4f22-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d4f22-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

