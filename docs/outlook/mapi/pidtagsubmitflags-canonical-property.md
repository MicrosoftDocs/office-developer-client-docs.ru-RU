---
title: Каноническое свойство PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339356"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="a5d4a-103">Каноническое свойство PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="a5d4a-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a5d4a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5d4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5d4a-105">Содержит битовую маску флагов, указывающих сведения об отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5d4a-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="a5d4a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a5d4a-107">ПР_СУБМИТ_ФЛАГС</span><span class="sxs-lookup"><span data-stu-id="a5d4a-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a5d4a-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="a5d4a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a5d4a-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="a5d4a-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="a5d4a-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a5d4a-110">Data type:</span></span>  <br/> |<span data-ttu-id="a5d4a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a5d4a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a5d4a-112">Область:</span><span class="sxs-lookup"><span data-stu-id="a5d4a-112">Area:</span></span>  <br/> |<span data-ttu-id="a5d4a-113">Несъемный MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d4a-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5d4a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5d4a-114">Remarks</span></span>

<span data-ttu-id="a5d4a-115">Для битовой маски **пр_субмит_флагс** можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="a5d4a-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="a5d4a-116">СУБМИТФЛАГ_ЛОККЕД</span><span class="sxs-lookup"><span data-stu-id="a5d4a-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="a5d4a-117">В настоящий момент сообщение заблокировано диспетчером очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="a5d4a-118">СУБМИТФЛАГ_ПРЕПРОЦЕСС</span><span class="sxs-lookup"><span data-stu-id="a5d4a-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="a5d4a-119">Сообщение нуждается в предварительной обработке.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-119">The message needs preprocessing.</span></span> <span data-ttu-id="a5d4a-120">Когда диспетчер очереди MAPI закончит предварительную обработку этого сообщения, он должен вызвать метод [iMessage:: субмитмессаже](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d4a-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="a5d4a-121">Поставщик хранилища сообщений распознает, что диспетчер очереди, а не клиентское приложение называется **субмитмессаже**, очищает флаг и продолжает отправку сообщения.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="a5d4a-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a5d4a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a5d4a-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a5d4a-123">Protocol specifications</span></span>

<span data-ttu-id="a5d4a-124">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5d4a-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5d4a-125">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a5d4a-126">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a5d4a-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a5d4a-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a5d4a-128">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="a5d4a-128">Header files</span></span>

<span data-ttu-id="a5d4a-129">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="a5d4a-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a5d4a-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a5d4a-131">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="a5d4a-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a5d4a-132">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="a5d4a-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a5d4a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="a5d4a-133">See also</span></span>



[<span data-ttu-id="a5d4a-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="a5d4a-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="a5d4a-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d4a-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a5d4a-136">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d4a-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a5d4a-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a5d4a-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a5d4a-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a5d4a-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

