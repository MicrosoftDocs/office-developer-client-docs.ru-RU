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
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="6d8b8-103">Каноническое свойство PidTagMessageDownloadTime</span><span class="sxs-lookup"><span data-stu-id="6d8b8-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="6d8b8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d8b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d8b8-105">Содержит предполагаемое время для загрузки сообщения с удаленного сервера в локальное хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d8b8-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d8b8-107">ПР_МЕССАЖЕ_ДОВНЛОАД_ТИМЕ</span><span class="sxs-lookup"><span data-stu-id="6d8b8-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="6d8b8-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d8b8-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="6d8b8-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="6d8b8-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d8b8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6d8b8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6d8b8-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d8b8-112">Area:</span></span>  <br/> |<span data-ttu-id="6d8b8-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="6d8b8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d8b8-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d8b8-114">Remarks</span></span>

<span data-ttu-id="6d8b8-115">Это свойство выражается в секундах и представляет собой наилучшую оценку времени, в течение которого он получит доступ к удаленному поставщику транспорта, чтобы скачать данное сообщение из текущего расположения в хранилище сообщений, локальное на клиенте, просматривая папку заголовков.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="6d8b8-116">Удаленный поставщик транспорта обычно вычисляет значение этого свойства, путем деления значения свойства **пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) на скорость канала связи (байт в секунду).</span><span class="sxs-lookup"><span data-stu-id="6d8b8-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="6d8b8-117">Если поставщик не может рассчитать время загрузки, например, если он не знает скорость связи, он должен указать значение **пт_еррор** , например **мапи_е_но_суппорт** для этого столбца в таблице содержимое папки заголовков.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6d8b8-118">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d8b8-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d8b8-119">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6d8b8-119">Header files</span></span>

<span data-ttu-id="6d8b8-120">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6d8b8-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d8b8-121">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d8b8-122">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6d8b8-122">Mapitags.h</span></span>
  
> <span data-ttu-id="6d8b8-123">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="6d8b8-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d8b8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6d8b8-124">See also</span></span>



[<span data-ttu-id="6d8b8-125">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8b8-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d8b8-126">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8b8-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d8b8-127">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d8b8-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d8b8-128">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d8b8-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

