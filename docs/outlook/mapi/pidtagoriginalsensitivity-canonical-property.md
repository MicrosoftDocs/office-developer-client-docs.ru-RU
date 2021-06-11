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
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="b5334-103">Каноническое свойство PidTagOriginalSensitivity</span><span class="sxs-lookup"><span data-stu-id="b5334-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="b5334-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5334-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5334-105">Содержит значение чувствительности, назначенное отправителю первой версии сообщения, то есть сообщение перед отправкой или ответом на него.</span><span class="sxs-lookup"><span data-stu-id="b5334-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5334-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b5334-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5334-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="b5334-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="b5334-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b5334-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5334-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="b5334-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="b5334-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b5334-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5334-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b5334-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b5334-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b5334-112">Area:</span></span>  <br/> |<span data-ttu-id="b5334-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="b5334-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5334-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5334-114">Remarks</span></span>

<span data-ttu-id="b5334-115">Клиентская заявка должна установить это свойство в том же значении, **что и свойство PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)при первом отправлении сообщения.</span><span class="sxs-lookup"><span data-stu-id="b5334-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="b5334-116">Его не следует менять впоследствии.</span><span class="sxs-lookup"><span data-stu-id="b5334-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="b5334-117">Это свойство используется поставщиком транспорта для защиты конфиденциальности скопированные записи.</span><span class="sxs-lookup"><span data-stu-id="b5334-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="b5334-118">Это позволяет, например, блокировать изменение исходного текста сообщения в форварде или отвечать на сообщение, которое изначально было отмечено **SENSITIVITY_PRIVATE**.</span><span class="sxs-lookup"><span data-stu-id="b5334-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5334-119">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5334-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b5334-120">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="b5334-120">Protocol specifications</span></span>

<span data-ttu-id="b5334-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5334-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5334-122">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="b5334-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b5334-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b5334-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b5334-124">Указывает свойства и операции, допустимые на объектах сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b5334-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b5334-125">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="b5334-125">Header files</span></span>

<span data-ttu-id="b5334-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5334-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5334-127">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b5334-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5334-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b5334-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b5334-129">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b5334-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5334-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b5334-130">See also</span></span>



[<span data-ttu-id="b5334-131">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5334-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5334-132">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b5334-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5334-133">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b5334-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5334-134">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="b5334-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

