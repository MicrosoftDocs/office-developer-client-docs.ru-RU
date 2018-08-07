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
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811357"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="d6c50-103">Каноническое свойство PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="d6c50-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="d6c50-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6c50-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6c50-105">Содержит предполагаемое время для загрузки сообщения с удаленного сервера в хранилище локального сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6c50-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6c50-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d6c50-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d6c50-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="d6c50-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="d6c50-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d6c50-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d6c50-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="d6c50-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="d6c50-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d6c50-110">Data type:</span></span>  <br/> |<span data-ttu-id="d6c50-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d6c50-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d6c50-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d6c50-112">Area:</span></span>  <br/> |<span data-ttu-id="d6c50-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="d6c50-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6c50-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d6c50-114">Remarks</span></span>

<span data-ttu-id="d6c50-115">Это свойство выражается в секундах и представляет наилучшую оценку времени, потребуется поставщик удаленного транспорта для загрузки данного сообщения из текущего места для хранения сообщений локальной папке заголовка клиенту.</span><span class="sxs-lookup"><span data-stu-id="d6c50-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="d6c50-116">Поставщик удаленного транспорта обычно рассчитываются значение для этого свойства значение свойства **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)), скорость канала связи в байтах в секунду.</span><span class="sxs-lookup"><span data-stu-id="d6c50-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="d6c50-117">Если поставщик не удается вычислить время загрузки, например, если не известно, скорость соединения, его следует предоставлять **PT_ERROR** значение например **MAPI_E_NO_SUPPORT** для этого столбца в таблице содержимое папки заголовок.</span><span class="sxs-lookup"><span data-stu-id="d6c50-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d6c50-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d6c50-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d6c50-119">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d6c50-119">Header files</span></span>

<span data-ttu-id="d6c50-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d6c50-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="d6c50-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d6c50-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="d6c50-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d6c50-122">Mapitags.h</span></span>
  
> <span data-ttu-id="d6c50-123">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="d6c50-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d6c50-124">См. также</span><span class="sxs-lookup"><span data-stu-id="d6c50-124">See also</span></span>



[<span data-ttu-id="d6c50-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6c50-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d6c50-126">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d6c50-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d6c50-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d6c50-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d6c50-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d6c50-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

