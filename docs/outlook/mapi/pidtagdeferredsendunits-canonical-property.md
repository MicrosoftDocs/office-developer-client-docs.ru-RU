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
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="f3c5c-103">Каноническое свойство PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="f3c5c-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="f3c5c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3c5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3c5c-105">Указывает единицу времени, на которую необходимо умножить значение свойства **пр_деферред_сенд_нумбер** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3c5c-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3c5c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f3c5c-107">ПР_ДЕФЕРРЕД_СЕНД_УНИТС</span><span class="sxs-lookup"><span data-stu-id="f3c5c-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="f3c5c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f3c5c-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="f3c5c-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="f3c5c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="f3c5c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f3c5c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f3c5c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-112">Area:</span></span>  <br/> |<span data-ttu-id="f3c5c-113">Состояние MAPI</span><span class="sxs-lookup"><span data-stu-id="f3c5c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3c5c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f3c5c-114">Remarks</span></span>

<span data-ttu-id="f3c5c-115">Если задано, это свойство должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f3c5c-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f3c5c-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="f3c5c-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="f3c5c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f3c5c-117">Description</span></span>  <br/> |
|<span data-ttu-id="f3c5c-118">нуль</span><span class="sxs-lookup"><span data-stu-id="f3c5c-118">0</span></span>  <br/> |<span data-ttu-id="f3c5c-119">Минут, например 60 секунды</span><span class="sxs-lookup"><span data-stu-id="f3c5c-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="f3c5c-120">1,1</span><span class="sxs-lookup"><span data-stu-id="f3c5c-120">1</span></span>  <br/> |<span data-ttu-id="f3c5c-121">Часы, например 60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="f3c5c-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f3c5c-122">2</span><span class="sxs-lookup"><span data-stu-id="f3c5c-122">2</span></span>  <br/> |<span data-ttu-id="f3c5c-123">День, например 24x60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="f3c5c-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="f3c5c-124">4</span><span class="sxs-lookup"><span data-stu-id="f3c5c-124">3</span></span>  <br/> |<span data-ttu-id="f3c5c-125">Неделя, например 7x24x60x60 секунды</span><span class="sxs-lookup"><span data-stu-id="f3c5c-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f3c5c-126">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f3c5c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f3c5c-127">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f3c5c-127">Protocol specifications</span></span>

<span data-ttu-id="f3c5c-128">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3c5c-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f3c5c-129">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f3c5c-130">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="f3c5c-130">Header files</span></span>

<span data-ttu-id="f3c5c-131">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="f3c5c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f3c5c-132">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f3c5c-133">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="f3c5c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f3c5c-134">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="f3c5c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3c5c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f3c5c-135">See also</span></span>



[<span data-ttu-id="f3c5c-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f3c5c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f3c5c-137">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="f3c5c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f3c5c-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f3c5c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f3c5c-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f3c5c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

