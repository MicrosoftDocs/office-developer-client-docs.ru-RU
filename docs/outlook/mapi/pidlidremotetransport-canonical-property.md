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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285181"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="9c331-103">Каноническое свойство PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="9c331-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="9c331-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c331-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c331-105">Определяет учетную запись, с которой связан элемент заголовка, в первую очередь для реализации функции POP на сервере.</span><span class="sxs-lookup"><span data-stu-id="9c331-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c331-106">Связанные свойства</span><span class="sxs-lookup"><span data-stu-id="9c331-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="9c331-107">Диспидремотексп</span><span class="sxs-lookup"><span data-stu-id="9c331-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="9c331-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="9c331-108">Property set:</span></span>  <br/> |<span data-ttu-id="9c331-109">Псетид_ремоте</span><span class="sxs-lookup"><span data-stu-id="9c331-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="9c331-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="9c331-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="9c331-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="9c331-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="9c331-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="9c331-112">Data type:</span></span>  <br/> |<span data-ttu-id="9c331-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="9c331-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="9c331-114">Область:</span><span class="sxs-lookup"><span data-stu-id="9c331-114">Area:</span></span>  <br/> |<span data-ttu-id="9c331-115">Удаленное сообщение</span><span class="sxs-lookup"><span data-stu-id="9c331-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c331-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="9c331-116">Remarks</span></span>

<span data-ttu-id="9c331-117">Это свойство относится только к сообщениям, у которых есть класс сообщения IPM. Удаленного.</span><span class="sxs-lookup"><span data-stu-id="9c331-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="9c331-118">В Microsoft Outlook поддерживается сопоставление различных учетных записей, которые загружаются в заданное хранилище в сообщении со сведениями о папке (ФАИ), но эти сведения также могут храниться в реестре.</span><span class="sxs-lookup"><span data-stu-id="9c331-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9c331-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9c331-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9c331-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="9c331-120">Protocol specifications</span></span>

<span data-ttu-id="9c331-121">[[MS — ОКСПРОПС]]</span><span class="sxs-lookup"><span data-stu-id="9c331-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="9c331-122">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="9c331-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9c331-123">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="9c331-123">Header files</span></span>

<span data-ttu-id="9c331-124">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9c331-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9c331-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="9c331-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c331-126">См. также</span><span class="sxs-lookup"><span data-stu-id="9c331-126">See also</span></span>



[<span data-ttu-id="9c331-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="9c331-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9c331-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="9c331-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9c331-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="9c331-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9c331-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="9c331-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

