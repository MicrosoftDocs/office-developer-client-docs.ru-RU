---
title: Каноническое свойство PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439445"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="c8f5e-103">Каноническое свойство PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="c8f5e-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="c8f5e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8f5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8f5e-105">Определяет, с какой учетной записью связан элемент загона, в первую очередь для реализации функции POP Leave on Server.</span><span class="sxs-lookup"><span data-stu-id="c8f5e-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8f5e-106">Связанные свойства</span><span class="sxs-lookup"><span data-stu-id="c8f5e-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="c8f5e-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="c8f5e-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="c8f5e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c8f5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="c8f5e-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="c8f5e-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="c8f5e-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c8f5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c8f5e-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="c8f5e-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="c8f5e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c8f5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="c8f5e-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c8f5e-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c8f5e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c8f5e-114">Area:</span></span>  <br/> |<span data-ttu-id="c8f5e-115">Удаленное сообщение</span><span class="sxs-lookup"><span data-stu-id="c8f5e-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8f5e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8f5e-116">Remarks</span></span>

<span data-ttu-id="c8f5e-117">Это свойство актуально только для сообщений, которые имеют класс сообщений IPM. Удаленный.</span><span class="sxs-lookup"><span data-stu-id="c8f5e-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="c8f5e-118">Корпорация Outlook сохраняет сопоставление различных учетных записей, скачиваемых в данный магазин, в сообщении о связанных с папками сведениях (FAI), но может также хранить эти сведения в реестре.</span><span class="sxs-lookup"><span data-stu-id="c8f5e-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c8f5e-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c8f5e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c8f5e-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c8f5e-120">Protocol specifications</span></span>

<span data-ttu-id="c8f5e-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="c8f5e-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="c8f5e-122">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="c8f5e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c8f5e-123">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="c8f5e-123">Header files</span></span>

<span data-ttu-id="c8f5e-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c8f5e-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="c8f5e-125">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c8f5e-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8f5e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="c8f5e-126">See also</span></span>



[<span data-ttu-id="c8f5e-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8f5e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c8f5e-128">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c8f5e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c8f5e-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c8f5e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c8f5e-130">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="c8f5e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

