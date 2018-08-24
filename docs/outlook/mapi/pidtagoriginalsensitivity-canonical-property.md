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
ms.openlocfilehash: 3c921d2c9eee69148713408ec2e2a5510a27011a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582709"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="f17f3-103">Каноническое свойство PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="f17f3-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="f17f3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f17f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f17f3-105">Со значением, назначенные отправителем первая версия сообщение содержит то есть сообщение перед пересылку и ответ.</span><span class="sxs-lookup"><span data-stu-id="f17f3-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f17f3-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f17f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f17f3-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="f17f3-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="f17f3-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f17f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f17f3-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="f17f3-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="f17f3-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f17f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="f17f3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f17f3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f17f3-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f17f3-112">Area:</span></span>  <br/> |<span data-ttu-id="f17f3-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="f17f3-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f17f3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f17f3-114">Remarks</span></span>

<span data-ttu-id="f17f3-115">Клиентское приложение следует этому свойству присвоено значение такое же значение как свойство **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) при первом сообщения.</span><span class="sxs-lookup"><span data-stu-id="f17f3-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="f17f3-116">Оно должно быть задано впоследствии.</span><span class="sxs-lookup"><span data-stu-id="f17f3-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="f17f3-117">Это свойство используется поставщик транспорта для защиты конфиденциальности на скопированной записи.</span><span class="sxs-lookup"><span data-stu-id="f17f3-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="f17f3-118">Включение его, например, для блокировки изменения исходного текста сообщения в прямого из или в ответ на сообщение, которое изначально помечено **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="f17f3-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f17f3-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f17f3-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f17f3-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f17f3-120">Protocol specifications</span></span>

<span data-ttu-id="f17f3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f17f3-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f17f3-122">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f17f3-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f17f3-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f17f3-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f17f3-124">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f17f3-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f17f3-125">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f17f3-125">Header files</span></span>

<span data-ttu-id="f17f3-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f17f3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f17f3-127">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f17f3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="f17f3-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f17f3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="f17f3-129">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f17f3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f17f3-130">См. также</span><span class="sxs-lookup"><span data-stu-id="f17f3-130">See also</span></span>



[<span data-ttu-id="f17f3-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f17f3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f17f3-132">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f17f3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f17f3-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f17f3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f17f3-134">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f17f3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

