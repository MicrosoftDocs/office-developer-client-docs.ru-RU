---
title: Каноническое свойство PidTagOriginalSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubmitTime
api_type:
- COM
ms.assetid: 2e027c0c-2370-437a-ad98-2bbb5e41e525
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 31324dff3c5780f693b1dc055fc2067436496cd3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573651"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="acb90-103">Каноническое свойство PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="acb90-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="acb90-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acb90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acb90-105">Содержит исходный отправки дату и время сообщения в отчете.</span><span class="sxs-lookup"><span data-stu-id="acb90-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="acb90-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="acb90-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="acb90-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="acb90-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="acb90-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="acb90-108">Identifier:</span></span>  <br/> |<span data-ttu-id="acb90-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="acb90-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="acb90-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="acb90-110">Data type:</span></span>  <br/> |<span data-ttu-id="acb90-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="acb90-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="acb90-112">Область:</span><span class="sxs-lookup"><span data-stu-id="acb90-112">Area:</span></span>  <br/> |<span data-ttu-id="acb90-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="acb90-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb90-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="acb90-114">Remarks</span></span>

<span data-ttu-id="acb90-115">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="acb90-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="acb90-116">Не изменяется при переслать сообщение.</span><span class="sxs-lookup"><span data-stu-id="acb90-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="acb90-117">Используется в отчетах только.</span><span class="sxs-lookup"><span data-stu-id="acb90-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="acb90-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="acb90-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="acb90-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="acb90-119">Protocol specifications</span></span>

<span data-ttu-id="acb90-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acb90-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acb90-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="acb90-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="acb90-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="acb90-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="acb90-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="acb90-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="acb90-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="acb90-124">Header files</span></span>

<span data-ttu-id="acb90-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="acb90-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="acb90-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="acb90-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="acb90-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="acb90-127">Mapitags.h</span></span>
  
> <span data-ttu-id="acb90-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="acb90-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acb90-129">См. также</span><span class="sxs-lookup"><span data-stu-id="acb90-129">See also</span></span>



[<span data-ttu-id="acb90-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="acb90-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="acb90-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="acb90-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="acb90-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="acb90-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="acb90-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="acb90-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

