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
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587119"
---
# <a name="pidlidremotetransport-canonical-property"></a><span data-ttu-id="74f93-103">Каноническое свойство PidLidRemoteTransport</span><span class="sxs-lookup"><span data-stu-id="74f93-103">PidLidRemoteTransport Canonical Property</span></span>

  
  
<span data-ttu-id="74f93-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74f93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74f93-105">Определяет, какая учетная запись элемент заголовка связан с, в основном для реализации оставлять POP на функциональность сервера.</span><span class="sxs-lookup"><span data-stu-id="74f93-105">Identifies what account the header item is associated with, primarily to implement the POP Leave on Server functionality.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74f93-106">Связанными свойствами</span><span class="sxs-lookup"><span data-stu-id="74f93-106">Associated Properties</span></span>  <br/> |<span data-ttu-id="74f93-107">dispidRemoteXP</span><span class="sxs-lookup"><span data-stu-id="74f93-107">dispidRemoteXP</span></span>  <br/> |
|<span data-ttu-id="74f93-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="74f93-108">Property set:</span></span>  <br/> |<span data-ttu-id="74f93-109">PSETID_Remote</span><span class="sxs-lookup"><span data-stu-id="74f93-109">PSETID_Remote</span></span>  <br/> |
|<span data-ttu-id="74f93-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="74f93-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="74f93-111">0x00008F03</span><span class="sxs-lookup"><span data-stu-id="74f93-111">0x00008F03</span></span>  <br/> |
|<span data-ttu-id="74f93-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="74f93-112">Data type:</span></span>  <br/> |<span data-ttu-id="74f93-113">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="74f93-113">PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="74f93-114">Область:</span><span class="sxs-lookup"><span data-stu-id="74f93-114">Area:</span></span>  <br/> |<span data-ttu-id="74f93-115">Удаленные сообщения</span><span class="sxs-lookup"><span data-stu-id="74f93-115">Remote message</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74f93-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="74f93-116">Remarks</span></span>

<span data-ttu-id="74f93-117">Это свойство является релевантным только на сообщения, для которых классом сообщений IPM. Удаленный.</span><span class="sxs-lookup"><span data-stu-id="74f93-117">This property is relevant only on messages that have a message class of IPM.Remote.</span></span> <span data-ttu-id="74f93-118">Microsoft Outlook сохраняет сопоставление различные учетные записи, которые загружаются для заданного хранилища в сообщении связанные сведения о папке (FAI), но она может синхронизировать эту информацию в реестре.</span><span class="sxs-lookup"><span data-stu-id="74f93-118">Microsoft Outlook keeps a mapping of various accounts that are downloading to a given store in a Folder Associated Information (FAI) message, but it could also keep this information in the registry.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="74f93-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="74f93-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="74f93-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="74f93-120">Protocol specifications</span></span>

<span data-ttu-id="74f93-121">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="74f93-121">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="74f93-122">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="74f93-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="74f93-123">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="74f93-123">Header files</span></span>

<span data-ttu-id="74f93-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="74f93-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="74f93-125">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="74f93-125">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="74f93-126">См. также</span><span class="sxs-lookup"><span data-stu-id="74f93-126">See also</span></span>



[<span data-ttu-id="74f93-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74f93-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="74f93-128">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="74f93-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="74f93-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="74f93-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="74f93-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="74f93-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

