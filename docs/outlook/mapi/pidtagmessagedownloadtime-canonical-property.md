---
title: Каноническое свойство PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407930"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="0502e-103">Каноническое свойство PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="0502e-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="0502e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0502e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0502e-105">Содержит предполагаемое время для загрузки сообщения с удаленного сервера в локальный магазин сообщений.</span><span class="sxs-lookup"><span data-stu-id="0502e-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0502e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0502e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0502e-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="0502e-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="0502e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0502e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0502e-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="0502e-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="0502e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0502e-110">Data type:</span></span>  <br/> |<span data-ttu-id="0502e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0502e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0502e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="0502e-112">Area:</span></span>  <br/> |<span data-ttu-id="0502e-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="0502e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0502e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0502e-114">Remarks</span></span>

<span data-ttu-id="0502e-115">Это свойство выражается в секундах и представляет собой лучшую оценку времени, которое может занять удаленное транспортное сообщение для загрузки данного сообщения из текущего расположения в локальный магазин сообщений для клиента, просматриваемого в папке загона.</span><span class="sxs-lookup"><span data-stu-id="0502e-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="0502e-116">Поставщик удаленного транспорта обычно вычисляет значение для этого свойства **путем** деления значения свойства [PR_MESSAGE_SIZE (PidTagMessageSize)](pidtagmessagesize-canonical-property.md)на скорость соединения сообщений в bytes в секунду.</span><span class="sxs-lookup"><span data-stu-id="0502e-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="0502e-117">Если поставщик не может рассчитать время загрузки, например, если он не  знает скорость ссылки, он должен предоставить значение PT_ERROR, например MAPI_E_NO_SUPPORT для этого столбца в таблице содержимого папки главы. </span><span class="sxs-lookup"><span data-stu-id="0502e-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0502e-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0502e-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0502e-119">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="0502e-119">Header files</span></span>

<span data-ttu-id="0502e-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0502e-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="0502e-121">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0502e-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="0502e-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0502e-122">Mapitags.h</span></span>
  
> <span data-ttu-id="0502e-123">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="0502e-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0502e-124">См. также</span><span class="sxs-lookup"><span data-stu-id="0502e-124">See also</span></span>



[<span data-ttu-id="0502e-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0502e-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0502e-126">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0502e-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0502e-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="0502e-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0502e-128">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="0502e-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

