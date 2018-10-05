---
title: Каноническое свойство PidTagOriginalSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 771a7c9cdf37a94875c881d8d7e8fd292893a0ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401484"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="c6675-103">Каноническое свойство PidTagOriginalSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="c6675-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="c6675-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6675-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6675-105">Содержит отображаемое имя системы обмена сообщениями пользователя, от чьего имени исходное сообщение было отправлено.</span><span class="sxs-lookup"><span data-stu-id="c6675-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c6675-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c6675-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6675-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="c6675-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="c6675-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c6675-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6675-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="c6675-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="c6675-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c6675-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6675-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c6675-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c6675-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c6675-112">Area:</span></span>  <br/> |<span data-ttu-id="c6675-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="c6675-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6675-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6675-114">Remarks</span></span>

<span data-ttu-id="c6675-115">В этих примерах свойства свойств адреса для исходного представленного отправителя сообщения.</span><span class="sxs-lookup"><span data-stu-id="c6675-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="c6675-116">Он используется в потоке беседы.</span><span class="sxs-lookup"><span data-stu-id="c6675-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="c6675-117">Клиентское приложение отправку сообщения от имени другого клиента эти свойства присвоено значение свойства **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) в первой отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="c6675-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="c6675-118">После установки, оно должно быть задано.</span><span class="sxs-lookup"><span data-stu-id="c6675-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c6675-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c6675-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6675-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c6675-120">Protocol specifications</span></span>

<span data-ttu-id="c6675-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6675-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6675-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c6675-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6675-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6675-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6675-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c6675-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6675-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c6675-125">Header files</span></span>

<span data-ttu-id="c6675-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c6675-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6675-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c6675-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6675-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c6675-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c6675-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c6675-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6675-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c6675-130">See also</span></span>



[<span data-ttu-id="c6675-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c6675-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6675-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c6675-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6675-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c6675-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6675-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c6675-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

