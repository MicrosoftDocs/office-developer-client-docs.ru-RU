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
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810524"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="24fad-103">Каноническое свойство PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="24fad-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="24fad-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="24fad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="24fad-105">Определяет, какая учетная запись элемент заголовка связан с, в основном для реализации оставлять POP на функциональность сервера.</span><span class="sxs-lookup"><span data-stu-id="24fad-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24fad-106">Связанными свойствами</span><span class="sxs-lookup"><span data-stu-id="24fad-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="24fad-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="24fad-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="24fad-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="24fad-108">Property set:</span></span>  <br/> |<span data-ttu-id="24fad-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="24fad-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="24fad-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="24fad-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="24fad-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="24fad-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="24fad-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="24fad-112">Data type:</span></span>  <br/> |<span data-ttu-id="24fad-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="24fad-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="24fad-114">Область:</span><span class="sxs-lookup"><span data-stu-id="24fad-114">Area:</span></span>  <br/> |<span data-ttu-id="24fad-115">Удаленные сообщения</span><span class="sxs-lookup"><span data-stu-id="24fad-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24fad-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="24fad-116">Remarks</span></span>

<span data-ttu-id="24fad-117">Это свойство является релевантным только на сообщения, для которых классом сообщений IPM. Удаленный.</span><span class="sxs-lookup"><span data-stu-id="24fad-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="24fad-118">Microsoft Outlook сохраняет сопоставление различные учетные записи, которые загружаются для заданного хранилища в сообщении связанные сведения о папке (FAI), но она может синхронизировать эту информацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="24fad-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="24fad-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="24fad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24fad-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="24fad-120">Protocol specifications</span></span>

<span data-ttu-id="24fad-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="24fad-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="24fad-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="24fad-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24fad-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="24fad-123">Header files</span></span>

<span data-ttu-id="24fad-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="24fad-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="24fad-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="24fad-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24fad-126">См. также</span><span class="sxs-lookup"><span data-stu-id="24fad-126">See also</span></span>



[<span data-ttu-id="24fad-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24fad-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24fad-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="24fad-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24fad-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="24fad-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24fad-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="24fad-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

