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
ms.openlocfilehash: 07aea33f54a29d497646b62f1f8bd96a383cbd7b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385734"
---
# <a name="pidtagoriginalsubmittime-canonical-property"></a><span data-ttu-id="f9e00-103">Каноническое свойство PidTagOriginalSubmitTime</span><span class="sxs-lookup"><span data-stu-id="f9e00-103">PidTagOriginalSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="f9e00-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9e00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9e00-105">Содержит исходный отправки дату и время сообщения в отчете.</span><span class="sxs-lookup"><span data-stu-id="f9e00-105">Contains the original submission date and time of the message in the report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9e00-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f9e00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f9e00-107">PR_ORIGINAL_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="f9e00-107">PR_ORIGINAL_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="f9e00-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f9e00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f9e00-109">0x004E</span><span class="sxs-lookup"><span data-stu-id="f9e00-109">0x004E</span></span>  <br/> |
|<span data-ttu-id="f9e00-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f9e00-110">Data type:</span></span>  <br/> |<span data-ttu-id="f9e00-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f9e00-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f9e00-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f9e00-112">Area:</span></span>  <br/> |<span data-ttu-id="f9e00-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="f9e00-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9e00-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9e00-114">Remarks</span></span>

<span data-ttu-id="f9e00-115">В первой отправки сообщения клиентское приложение следует этому свойству присвоено значение свойства **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f9e00-115">At first submission of a message, a client application should set this property to the value of the **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) property.</span></span> <span data-ttu-id="f9e00-116">Не изменяется при переслать сообщение.</span><span class="sxs-lookup"><span data-stu-id="f9e00-116">It is not changed when the message is forwarded.</span></span> <span data-ttu-id="f9e00-117">Используется в отчетах только.</span><span class="sxs-lookup"><span data-stu-id="f9e00-117">This is used in reports only.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f9e00-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f9e00-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f9e00-119">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f9e00-119">Protocol specifications</span></span>

<span data-ttu-id="f9e00-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9e00-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9e00-121">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f9e00-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f9e00-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f9e00-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f9e00-123">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f9e00-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f9e00-124">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f9e00-124">Header files</span></span>

<span data-ttu-id="f9e00-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f9e00-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f9e00-126">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f9e00-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f9e00-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f9e00-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f9e00-128">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f9e00-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9e00-129">См. также</span><span class="sxs-lookup"><span data-stu-id="f9e00-129">See also</span></span>



[<span data-ttu-id="f9e00-130">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f9e00-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f9e00-131">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f9e00-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f9e00-132">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f9e00-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f9e00-133">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f9e00-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

