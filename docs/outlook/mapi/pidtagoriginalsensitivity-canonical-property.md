---
title: Каноническое свойство PidTagOriginalSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341232"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="ae93c-103">Каноническое свойство PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="ae93c-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="ae93c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae93c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae93c-105">Содержит значение чувствительности, назначенное отправителем первой версии сообщения с сообщением перед пересылкой или ответом.</span><span class="sxs-lookup"><span data-stu-id="ae93c-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae93c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ae93c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ae93c-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="ae93c-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="ae93c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ae93c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ae93c-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="ae93c-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="ae93c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ae93c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ae93c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ae93c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ae93c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ae93c-112">Area:</span></span>  <br/> |<span data-ttu-id="ae93c-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="ae93c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae93c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae93c-114">Remarks</span></span>

<span data-ttu-id="ae93c-115">Клиентскому приложению следует задать для этого свойства то же значение, что и свойство **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) при первом отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="ae93c-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="ae93c-116">Его не следует изменять в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="ae93c-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="ae93c-117">Это свойство используется поставщиком транспорта для защиты чувствительности к скопированным записям.</span><span class="sxs-lookup"><span data-stu-id="ae93c-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="ae93c-118">Это позволяет, например, блокировать изменение текста исходного сообщения при пересылке или ответе на сообщение, изначально помеченное **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="ae93c-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ae93c-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ae93c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ae93c-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ae93c-120">Protocol specifications</span></span>

<span data-ttu-id="ae93c-121">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae93c-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae93c-122">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ae93c-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ae93c-123">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae93c-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ae93c-124">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ae93c-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ae93c-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ae93c-125">Header files</span></span>

<span data-ttu-id="ae93c-126">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ae93c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="ae93c-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ae93c-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="ae93c-128">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ae93c-128">Mapitags.h</span></span>
  
> <span data-ttu-id="ae93c-129">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ae93c-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ae93c-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ae93c-130">See also</span></span>



[<span data-ttu-id="ae93c-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ae93c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ae93c-132">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ae93c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ae93c-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ae93c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ae93c-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ae93c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

