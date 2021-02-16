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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320043"
---
# <a name="pidtagreadreceiptsearchkey-canonical-property"></a><span data-ttu-id="a5c9f-103">Каноническое свойство PidTagReadReceiptSearchKey</span><span class="sxs-lookup"><span data-stu-id="a5c9f-103">PidTagReadReceiptSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="a5c9f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5c9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5c9f-105">Содержит ключ поиска для пользователя обмена сообщениями, которому система обмена сообщениями должна направить отчет о прочтение сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-105">Contains a search key for the messaging user to which the messaging system should direct a read report for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c9f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5c9f-107">PR_READ_RECEIPT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="a5c9f-107">PR_READ_RECEIPT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="a5c9f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5c9f-109">0x0053</span><span class="sxs-lookup"><span data-stu-id="a5c9f-109">0x0053</span></span>  <br/> |
|<span data-ttu-id="a5c9f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5c9f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a5c9f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a5c9f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a5c9f-112">Area:</span></span>  <br/> |<span data-ttu-id="a5c9f-113">Конверт MAPI</span><span class="sxs-lookup"><span data-stu-id="a5c9f-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5c9f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5c9f-114">Remarks</span></span>

<span data-ttu-id="a5c9f-115">Это свойство игнорируется, если для свойства **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)не установлено значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-115">This property is ignored unless the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set to TRUE.</span></span>
  
<span data-ttu-id="a5c9f-116">Если клиентские приложения хотят получить отчеты о прочтении, оно может оставить это свойство ненастроенным или установить для него ключ поиска, содержащийся в свойстве **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)во время отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-116">If a client application wants to receive read reports itself, it can leave this property unset or set it to the search key contained in the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property at message submission time.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a5c9f-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5c9f-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5c9f-118">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5c9f-118">Protocol specifications</span></span>

<span data-ttu-id="a5c9f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5c9f-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5c9f-120">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5c9f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5c9f-121">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5c9f-122">Указывает свойства и операции, которые разрешены для сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-122">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5c9f-123">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="a5c9f-123">Header files</span></span>

<span data-ttu-id="a5c9f-124">Mapidef.h</span><span class="sxs-lookup"><span data-stu-id="a5c9f-124">Mapidef.h</span></span>
  
> <span data-ttu-id="a5c9f-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5c9f-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a5c9f-126">Mapitags.h</span></span>
  
> <span data-ttu-id="a5c9f-127">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="a5c9f-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5c9f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a5c9f-128">See also</span></span>



[<span data-ttu-id="a5c9f-129">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5c9f-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5c9f-130">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5c9f-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5c9f-131">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5c9f-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5c9f-132">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5c9f-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

