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
ms.openlocfilehash: b7e2db23b43383ca405ac58216b94a23d3257fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578341"
---
# <a name="pidlidautoprocessstate-canonical-property"></a><span data-ttu-id="ab865-103">Каноническое свойство PidLidAutoProcessState</span><span class="sxs-lookup"><span data-stu-id="ab865-103">PidLidAutoProcessState Canonical Property</span></span>

  
  
<span data-ttu-id="ab865-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab865-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab865-105">Задает параметры, которые используются в автоматической обработки сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ab865-105">Specifies the options that are used in automatic processing of email messages.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab865-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ab865-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab865-107">dispidSniffState</span><span class="sxs-lookup"><span data-stu-id="ab865-107">dispidSniffState</span></span>  <br/> |
|<span data-ttu-id="ab865-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ab865-108">Property set:</span></span>  <br/> |<span data-ttu-id="ab865-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="ab865-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="ab865-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ab865-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ab865-111">0x0000851A</span><span class="sxs-lookup"><span data-stu-id="ab865-111">0x0000851A</span></span>  <br/> |
|<span data-ttu-id="ab865-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ab865-112">Data type:</span></span>  <br/> |<span data-ttu-id="ab865-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab865-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab865-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ab865-114">Area:</span></span>  <br/> |<span data-ttu-id="ab865-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="ab865-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab865-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ab865-116">Remarks</span></span>

<span data-ttu-id="ab865-117">Свойство может отсутствовать, в противном случае используется значение по умолчанию «0x00000000».</span><span class="sxs-lookup"><span data-stu-id="ab865-117">The property may be absent, in which case the default value of "0x00000000" is used.</span></span> <span data-ttu-id="ab865-118">Если задано, это свойство должно быть присвоено одно из значений в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="ab865-118">If set, this property must be set to one of the values in the following table.</span></span>
  
|<span data-ttu-id="ab865-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ab865-119">**Value**</span></span>|<span data-ttu-id="ab865-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ab865-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ab865-121">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab865-121">0x00000000</span></span>  <br/> |<span data-ttu-id="ab865-122">Не обрабатывают сообщения автоматически.</span><span class="sxs-lookup"><span data-stu-id="ab865-122">Do not automatically process the message.</span></span>  <br/> |
|<span data-ttu-id="ab865-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ab865-123">0x00000001</span></span>  <br/> |<span data-ttu-id="ab865-124">Автоматически обрабатывать сообщения или при открытии сообщения.</span><span class="sxs-lookup"><span data-stu-id="ab865-124">Process the message automatically or when the message is opened.</span></span>  <br/> |
|<span data-ttu-id="ab865-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ab865-125">0x00000002</span></span>  <br/> |<span data-ttu-id="ab865-126">Процесс сообщения только при открытии сообщения.</span><span class="sxs-lookup"><span data-stu-id="ab865-126">Process the message only when the message is opened.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ab865-127">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ab865-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab865-128">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ab865-128">Protocol specifications</span></span>

<span data-ttu-id="ab865-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab865-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab865-130">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ab865-130">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ab865-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab865-131">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab865-132">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ab865-132">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab865-133">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ab865-133">Header files</span></span>

<span data-ttu-id="ab865-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab865-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab865-135">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ab865-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab865-136">См. также</span><span class="sxs-lookup"><span data-stu-id="ab865-136">See also</span></span>



[<span data-ttu-id="ab865-137">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ab865-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab865-138">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ab865-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab865-139">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ab865-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab865-140">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ab865-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

