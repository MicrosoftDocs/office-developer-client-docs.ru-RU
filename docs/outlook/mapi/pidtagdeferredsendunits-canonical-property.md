---
title: Каноническое свойство PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359908"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="6addd-103">Каноническое свойство PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="6addd-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="6addd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6addd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6addd-105">Указывает единицу времени, на которое должно умножаться значение свойства **PR_DEFERRED_SEND_NUMBER** [(PidTagDeferredSendNumber).](pidtagdeferredsendnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6addd-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6addd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6addd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6addd-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="6addd-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="6addd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6addd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6addd-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="6addd-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="6addd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6addd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6addd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6addd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6addd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6addd-112">Area:</span></span>  <br/> |<span data-ttu-id="6addd-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="6addd-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6addd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6addd-114">Remarks</span></span>

<span data-ttu-id="6addd-115">Если за установлено, это свойство должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6addd-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6addd-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="6addd-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="6addd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6addd-117">Description</span></span>  <br/> |
|<span data-ttu-id="6addd-118">0</span><span class="sxs-lookup"><span data-stu-id="6addd-118">0</span></span>  <br/> |<span data-ttu-id="6addd-119">Минуты, например 60 секунд</span><span class="sxs-lookup"><span data-stu-id="6addd-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="6addd-120">1 </span><span class="sxs-lookup"><span data-stu-id="6addd-120">1</span></span>  <br/> |<span data-ttu-id="6addd-121">Часы, например 60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="6addd-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="6addd-122">2 </span><span class="sxs-lookup"><span data-stu-id="6addd-122">2</span></span>  <br/> |<span data-ttu-id="6addd-123">День, например 24x60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="6addd-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="6addd-124">3 </span><span class="sxs-lookup"><span data-stu-id="6addd-124">3</span></span>  <br/> |<span data-ttu-id="6addd-125">Неделя, например 7x24x60x60 секунд</span><span class="sxs-lookup"><span data-stu-id="6addd-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6addd-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6addd-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6addd-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6addd-127">Protocol specifications</span></span>

<span data-ttu-id="6addd-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6addd-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6addd-129">Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6addd-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6addd-130">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6addd-130">Header files</span></span>

<span data-ttu-id="6addd-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6addd-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="6addd-132">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6addd-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="6addd-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6addd-133">Mapitags.h</span></span>
  
> <span data-ttu-id="6addd-134">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6addd-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6addd-135">См. также</span><span class="sxs-lookup"><span data-stu-id="6addd-135">See also</span></span>



[<span data-ttu-id="6addd-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6addd-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6addd-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6addd-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6addd-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6addd-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6addd-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6addd-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

