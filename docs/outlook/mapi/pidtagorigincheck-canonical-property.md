---
title: Каноническое свойство PidTagOriginCheck
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a82b1351c9d2d19c32e34b03a537a12bf93deb8a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435763"
---
# <a name="pidtagorigincheck-canonical-property"></a><span data-ttu-id="59950-103">Каноническое свойство PidTagOriginCheck</span><span class="sxs-lookup"><span data-stu-id="59950-103">PidTagOriginCheck Canonical Property</span></span>

  
  
<span data-ttu-id="59950-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59950-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59950-105">Содержит двоичное значение проверки, позволяющее получателю отчета о доставке проверять происхождение исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="59950-105">Contains a binary verification value that enables a delivery report recipient to verify the origin of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59950-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="59950-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59950-107">ПР_ОРИГИН_ЧЕКК</span><span class="sxs-lookup"><span data-stu-id="59950-107">PR_ORIGIN_CHECK</span></span>  <br/> |
|<span data-ttu-id="59950-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="59950-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59950-109">0x0027</span><span class="sxs-lookup"><span data-stu-id="59950-109">0x0027</span></span>  <br/> |
|<span data-ttu-id="59950-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="59950-110">Data type:</span></span>  <br/> |<span data-ttu-id="59950-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="59950-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="59950-112">Область:</span><span class="sxs-lookup"><span data-stu-id="59950-112">Area:</span></span>  <br/> |<span data-ttu-id="59950-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="59950-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59950-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="59950-114">Remarks</span></span>

<span data-ttu-id="59950-115">Это свойство предоставляет средства для третьей стороны, например агента передачи сообщений (MTA) или пользователя обмена сообщениями, получающего отчет о доставке, для проверки источника отправленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="59950-115">This property provides a means for a third party, such as a message transfer agent (MTA) or a messaging user receiving a delivery report, to verify the submitted message's origin.</span></span> <span data-ttu-id="59950-116">При наличии в полученном сообщении это свойство должно быть скопировано в отчет о доставке, созданный в ответ на сообщение.</span><span class="sxs-lookup"><span data-stu-id="59950-116">If present on a received message, this property should be copied onto any delivery report generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59950-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="59950-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="59950-118">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="59950-118">Header files</span></span>

<span data-ttu-id="59950-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="59950-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="59950-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="59950-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="59950-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="59950-121">Mapitags.h</span></span>
  
> <span data-ttu-id="59950-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="59950-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59950-123">См. также</span><span class="sxs-lookup"><span data-stu-id="59950-123">See also</span></span>



[<span data-ttu-id="59950-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="59950-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59950-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="59950-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59950-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="59950-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59950-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="59950-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

