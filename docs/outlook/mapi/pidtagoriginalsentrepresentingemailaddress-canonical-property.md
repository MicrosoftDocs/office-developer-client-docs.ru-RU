---
title: Каноническое свойство PidTagOriginalSentRepresentingEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e2c3d2c3-5451-45cb-b0ec-bdbf5b39a0ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2530e27993163505b28fa7d08fd5caf4cc9b03be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341190"
---
# <a name="pidtagoriginalsentrepresentingemailaddress-canonical-property"></a><span data-ttu-id="72190-103">Каноническое свойство PidTagOriginalSentRepresentingEmailAddress</span><span class="sxs-lookup"><span data-stu-id="72190-103">PidTagOriginalSentRepresentingEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="72190-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72190-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72190-105">Содержит адрес электронной почты пользователя обмена сообщениями, от имени которого было отправлено исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="72190-105">Contains the email address of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72190-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="72190-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72190-107">ПР_ОРИГИНАЛ_СЕНТ_РЕПРЕСЕНТИНГ_ЕМАИЛ_АДДРЕСС, ПР_ОРИГИНАЛ_СЕНТ_РЕПРЕСЕНТИНГ_ЕМАИЛ_АДДРЕСС_А, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="72190-107">PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_A, PR_ORIGINAL_SENT_REPRESENTING_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="72190-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="72190-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72190-109">0x0069</span><span class="sxs-lookup"><span data-stu-id="72190-109">0x0069</span></span>  <br/> |
|<span data-ttu-id="72190-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="72190-110">Data type:</span></span>  <br/> |<span data-ttu-id="72190-111">PT_STRING8, ПТ_УНИКОДЕ</span><span class="sxs-lookup"><span data-stu-id="72190-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="72190-112">Область:</span><span class="sxs-lookup"><span data-stu-id="72190-112">Area:</span></span>  <br/> |<span data-ttu-id="72190-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="72190-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72190-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72190-114">Remarks</span></span>

<span data-ttu-id="72190-115">Эти свойства являются примерами свойств Address для исходного предоставленного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="72190-115">These properties are examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="72190-116">Он используется в цепочке бесед.</span><span class="sxs-lookup"><span data-stu-id="72190-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="72190-117">Клиентское приложение, отправляющее сообщение от имени другого клиента, должно задать для этих свойств значение свойства **пр_сент_репресентинг_емаил_аддресс** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) при первой отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="72190-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="72190-118">После установки он не должен изменяться.</span><span class="sxs-lookup"><span data-stu-id="72190-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72190-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="72190-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72190-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="72190-120">Protocol specifications</span></span>

<span data-ttu-id="72190-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72190-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72190-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="72190-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72190-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72190-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72190-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="72190-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72190-125">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="72190-125">Header files</span></span>

<span data-ttu-id="72190-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="72190-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="72190-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="72190-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="72190-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="72190-128">Mapitags.h</span></span>
  
> <span data-ttu-id="72190-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="72190-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72190-130">См. также</span><span class="sxs-lookup"><span data-stu-id="72190-130">See also</span></span>



[<span data-ttu-id="72190-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="72190-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72190-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="72190-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72190-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="72190-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72190-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="72190-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

