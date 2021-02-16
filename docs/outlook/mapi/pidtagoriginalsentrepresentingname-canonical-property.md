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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341105"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="1a665-103">Каноническое свойство PidTagOriginalSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="1a665-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="1a665-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a665-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a665-105">Содержит отображаемую фамилию пользователя обмена сообщениями, от имени которого было отправлено исходное сообщение.</span><span class="sxs-lookup"><span data-stu-id="1a665-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a665-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1a665-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a665-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1a665-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="1a665-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1a665-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a665-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="1a665-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="1a665-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1a665-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a665-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a665-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1a665-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1a665-112">Area:</span></span>  <br/> |<span data-ttu-id="1a665-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="1a665-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a665-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a665-114">Remarks</span></span>

<span data-ttu-id="1a665-115">В этих примерах свойств адреса исходного представленного отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="1a665-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="1a665-116">Он используется в цепочке беседы.</span><span class="sxs-lookup"><span data-stu-id="1a665-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="1a665-117">Клиентские приложения, отправляющие сообщение от имени другого клиента, должны установить для этих свойств значение **свойства PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)при первой отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="1a665-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="1a665-118">После этого его не следует менять.</span><span class="sxs-lookup"><span data-stu-id="1a665-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1a665-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1a665-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a665-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1a665-120">Protocol specifications</span></span>

<span data-ttu-id="1a665-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a665-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a665-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="1a665-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1a665-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1a665-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1a665-124">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1a665-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a665-125">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="1a665-125">Header files</span></span>

<span data-ttu-id="1a665-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a665-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a665-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1a665-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a665-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a665-128">Mapitags.h</span></span>
  
> <span data-ttu-id="1a665-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1a665-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a665-130">См. также</span><span class="sxs-lookup"><span data-stu-id="1a665-130">See also</span></span>



[<span data-ttu-id="1a665-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a665-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a665-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1a665-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a665-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1a665-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a665-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1a665-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

