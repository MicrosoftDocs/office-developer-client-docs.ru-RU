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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356527"
---
# <a name="pidtagreadreceiptentryid-canonical-property"></a><span data-ttu-id="6aff4-103">Каноническое свойство PidTagReadReceiptEntryId</span><span class="sxs-lookup"><span data-stu-id="6aff4-103">PidTagReadReceiptEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6aff4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6aff4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6aff4-105">Содержит идентификатор записи для пользователя обмена сообщениями, в котором система обмена сообщениями должна направлять отчет о прочтение для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="6aff4-105">Contains an entry identifier for the messaging user where the messaging system should direct a read report for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6aff4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6aff4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6aff4-107">PR_READ_RECEIPT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6aff4-107">PR_READ_RECEIPT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6aff4-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6aff4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6aff4-109">0x0046</span><span class="sxs-lookup"><span data-stu-id="6aff4-109">0x0046</span></span>  <br/> |
|<span data-ttu-id="6aff4-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6aff4-110">Data type:</span></span>  <br/> |<span data-ttu-id="6aff4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6aff4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6aff4-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6aff4-112">Area:</span></span>  <br/> |<span data-ttu-id="6aff4-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="6aff4-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6aff4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6aff4-114">Remarks</span></span>

<span data-ttu-id="6aff4-115">Это свойство игнорируется, если **PR_READ_RECEIPT_REQUESTED** [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)свойство true.</span><span class="sxs-lookup"><span data-stu-id="6aff4-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="6aff4-116">Если клиентская заявка хочет получать отчеты о прочтении, она может оставить это свойство неустановленным или установить его в идентификатор записи, содержащийся в свойстве **PR_SENDER_ENTRYID** [(PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md)во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="6aff4-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the entry identifier contained in the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6aff4-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6aff4-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6aff4-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6aff4-118">Protocol specifications</span></span>

<span data-ttu-id="6aff4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6aff4-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6aff4-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="6aff4-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6aff4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6aff4-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6aff4-122">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6aff4-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6aff4-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6aff4-123">Header files</span></span>

<span data-ttu-id="6aff4-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6aff4-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6aff4-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6aff4-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6aff4-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6aff4-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6aff4-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6aff4-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6aff4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6aff4-128">See also</span></span>



[<span data-ttu-id="6aff4-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6aff4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6aff4-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6aff4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6aff4-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6aff4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6aff4-132">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6aff4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

