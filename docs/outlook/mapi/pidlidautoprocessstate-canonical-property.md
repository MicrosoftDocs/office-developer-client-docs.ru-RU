---
title: Каноническое свойство PidLidAutoProcessState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0918c15d87219c1ee20b177ae21e718e0289cf04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342065"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="85ad4-103">Каноническое свойство PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="85ad4-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="85ad4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85ad4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85ad4-105">Указывает параметры, используемые при автоматической обработке сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85ad4-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85ad4-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="85ad4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85ad4-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="85ad4-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="85ad4-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="85ad4-108">Property set:</span></span>  <br/> |<span data-ttu-id="85ad4-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="85ad4-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="85ad4-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="85ad4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="85ad4-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="85ad4-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="85ad4-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="85ad4-112">Data type:</span></span>  <br/> |<span data-ttu-id="85ad4-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="85ad4-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="85ad4-114">Область:</span><span class="sxs-lookup"><span data-stu-id="85ad4-114">Area:</span></span>  <br/> |<span data-ttu-id="85ad4-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="85ad4-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85ad4-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="85ad4-116">Remarks</span></span>

<span data-ttu-id="85ad4-117">Свойство может отсутствовать, в этом случае используется значение по умолчанию "0x00000000".</span><span class="sxs-lookup"><span data-stu-id="85ad4-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="85ad4-118">Если за установлено, этому свойству необходимо установить одно из значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="85ad4-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="85ad4-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="85ad4-119">**Value**</span></span>|<span data-ttu-id="85ad4-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="85ad4-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85ad4-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85ad4-121">0x00000000</span></span>  <br/> |<span data-ttu-id="85ad4-122">Не обработать сообщение автоматически.</span><span class="sxs-lookup"><span data-stu-id="85ad4-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="85ad4-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="85ad4-123">0x00000001</span></span>  <br/> |<span data-ttu-id="85ad4-124">Обработать сообщение автоматически или при его открытом.</span><span class="sxs-lookup"><span data-stu-id="85ad4-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="85ad4-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="85ad4-125">0x00000002</span></span>  <br/> |<span data-ttu-id="85ad4-126">Обработать сообщение, только когда сообщение открыто.</span><span class="sxs-lookup"><span data-stu-id="85ad4-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="85ad4-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="85ad4-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85ad4-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="85ad4-128">Protocol specifications</span></span>

<span data-ttu-id="85ad4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ad4-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ad4-130">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="85ad4-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85ad4-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85ad4-131">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85ad4-132">Указывает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="85ad4-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85ad4-133">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="85ad4-133">Header files</span></span>

<span data-ttu-id="85ad4-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85ad4-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="85ad4-135">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="85ad4-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85ad4-136">См. также</span><span class="sxs-lookup"><span data-stu-id="85ad4-136">See also</span></span>



[<span data-ttu-id="85ad4-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85ad4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85ad4-138">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="85ad4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85ad4-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="85ad4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85ad4-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="85ad4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

