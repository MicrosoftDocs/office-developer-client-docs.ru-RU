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
ms.openlocfilehash: 444d98c4e8e32e0cc7d2eb8af753a394af1f020c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811992"
---
# <a name="pidtagsubmitflags-canonical-property"></a><span data-ttu-id="c69df-103">Каноническое свойство PidTagSubmitFlags</span><span class="sxs-lookup"><span data-stu-id="c69df-103">PidTagSubmitFlags Canonical Property</span></span>

  
  
<span data-ttu-id="c69df-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c69df-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c69df-105">Содержит битовую маску флагов, указывающее, подробные сведения о отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="c69df-105">Contains a bitmask of flags indicating details about a message submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c69df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="c69df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c69df-107">PR_SUBMIT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c69df-107">PR_SUBMIT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c69df-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="c69df-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c69df-109">0x0E14</span><span class="sxs-lookup"><span data-stu-id="c69df-109">0x0E14</span></span>  <br/> |
|<span data-ttu-id="c69df-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c69df-110">Data type:</span></span>  <br/> |<span data-ttu-id="c69df-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c69df-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c69df-112">Область:</span><span class="sxs-lookup"><span data-stu-id="c69df-112">Area:</span></span>  <br/> |<span data-ttu-id="c69df-113">MAPI передаваемого</span><span class="sxs-lookup"><span data-stu-id="c69df-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c69df-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c69df-114">Remarks</span></span>

<span data-ttu-id="c69df-115">Один или несколько из следующих флагов можно задать для битовой маски **PR_SUBMIT_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="c69df-115">One or more of the following flags can be set for the **PR_SUBMIT_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="c69df-116">SUBMITFLAG_LOCKED</span><span class="sxs-lookup"><span data-stu-id="c69df-116">SUBMITFLAG_LOCKED</span></span> 
  
> <span data-ttu-id="c69df-117">Диспетчер очереди MAPI в настоящее время имеет сообщение блокируется.</span><span class="sxs-lookup"><span data-stu-id="c69df-117">The MAPI spooler currently has the message locked.</span></span> 
    
<span data-ttu-id="c69df-118">SUBMITFLAG_PREPROCESS</span><span class="sxs-lookup"><span data-stu-id="c69df-118">SUBMITFLAG_PREPROCESS</span></span> 
  
> <span data-ttu-id="c69df-119">Сообщение должно предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="c69df-119">The message needs preprocessing.</span></span> <span data-ttu-id="c69df-120">Когда выполняется диспетчер очереди MAPI предварительной обработки это сообщение, его необходимо вызвать метод [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="c69df-120">When the MAPI spooler is done preprocessing this message, it should call the [IMessage::SubmitMessage](imessage-submitmessage.md) method.</span></span> <span data-ttu-id="c69df-121">Поставщик хранения сообщений обнаруживает, что диспетчер очереди, а не клиентского приложения называется **SubmitMessage**, сбрасывает и по-прежнему производится передача сообщений.</span><span class="sxs-lookup"><span data-stu-id="c69df-121">The message store provider recognizes that the spooler, rather than the client application, has called **SubmitMessage**, clears the flag, and continues message submission.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c69df-122">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c69df-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c69df-123">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c69df-123">Protocol specifications</span></span>

<span data-ttu-id="c69df-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c69df-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c69df-125">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c69df-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c69df-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c69df-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c69df-127">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="c69df-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c69df-128">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="c69df-128">Header files</span></span>

<span data-ttu-id="c69df-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c69df-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c69df-130">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c69df-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c69df-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c69df-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c69df-132">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="c69df-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c69df-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c69df-133">See also</span></span>



[<span data-ttu-id="c69df-134">IMsgStore::SetLockState</span><span class="sxs-lookup"><span data-stu-id="c69df-134">IMsgStore::SetLockState</span></span>](imsgstore-setlockstate.md)


[<span data-ttu-id="c69df-135">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c69df-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c69df-136">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c69df-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c69df-137">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c69df-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c69df-138">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c69df-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

