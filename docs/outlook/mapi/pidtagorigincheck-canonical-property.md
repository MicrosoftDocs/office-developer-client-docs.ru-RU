---
title: Каноническое свойство PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811499"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="86a07-103">Каноническое свойство PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="86a07-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="86a07-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86a07-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86a07-105">Содержит значение двоичные проверки, которая позволяет получателя отчета доставки для проверки origin исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="86a07-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86a07-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="86a07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="86a07-107">PR_ORIGIN_CHECK</span><span class="sxs-lookup"><span data-stu-id="86a07-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="86a07-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="86a07-108">Identifier:</span></span>  <br/> |<span data-ttu-id="86a07-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="86a07-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="86a07-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="86a07-110">Data type:</span></span>  <br/> |<span data-ttu-id="86a07-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="86a07-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="86a07-112">Область:</span><span class="sxs-lookup"><span data-stu-id="86a07-112">Area:</span></span>  <br/> |<span data-ttu-id="86a07-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="86a07-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86a07-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="86a07-114">Remarks</span></span>

<span data-ttu-id="86a07-115">Это свойство предоставляет средства для сторонних производителей, такие как сообщения передачи (агента) или обмена мгновенными сообщениями пользователя получения отчетов о доставке, чтобы проверить источник отправляемого сообщения.</span><span class="sxs-lookup"><span data-stu-id="86a07-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="86a07-116">Если этот параметр указан, для полученного сообщения, это свойство должен быть скопирован на любой отчетов о доставке, возникающие в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="86a07-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="86a07-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="86a07-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="86a07-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="86a07-118">Header files</span></span>

<span data-ttu-id="86a07-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="86a07-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="86a07-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="86a07-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="86a07-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="86a07-121">Mapitags.h</span></span>
  
> <span data-ttu-id="86a07-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="86a07-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="86a07-123">См. также</span><span class="sxs-lookup"><span data-stu-id="86a07-123">See also</span></span>



[<span data-ttu-id="86a07-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="86a07-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="86a07-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="86a07-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="86a07-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="86a07-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="86a07-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="86a07-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

