---
title: Каноническое свойство PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357619"
---
# <a name="pidlidcustomflag-canonical-property"></a><span data-ttu-id="819df-103">Каноническое свойство PidLidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="819df-103">PidLidCustomFlag Canonical Property</span></span>

  
  
<span data-ttu-id="819df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="819df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="819df-105">Битмаска, которая указывает, как настраивается сообщение, например, сохранено с помощью настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="819df-105">A bitmask that specifies how a message is customized, for example, saved with custom properties.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="819df-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="819df-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="819df-107">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="819df-107">dispidCustomFlag</span></span>  <br/> |
|<span data-ttu-id="819df-108">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="819df-108">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="819df-109">0x00008251</span><span class="sxs-lookup"><span data-stu-id="819df-109">0x00008251</span></span>  <br/> |
|<span data-ttu-id="819df-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="819df-110">Data type:</span></span>  <br/> |<span data-ttu-id="819df-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="819df-111">PT_LONG</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="819df-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="819df-112">Remarks</span></span>

<span data-ttu-id="819df-113">Чтобы получить значение этого свойства, сначала используйте **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** для получения тега свойства, а затем укажите этот тег свойства в **[IMAPIProp::GetProps,](imapiprop-getprops.md)** чтобы получить значение.</span><span class="sxs-lookup"><span data-stu-id="819df-113">To retrieve the value of this property, first use **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** to obtain the property tag, and then specify this property tag in **[IMAPIProp::GetProps](imapiprop-getprops.md)** to get the value.</span></span> 
  
<span data-ttu-id="819df-114">Возможные флаги:</span><span class="sxs-lookup"><span data-stu-id="819df-114">Possible Flags are as follows:</span></span>
  
****

|<span data-ttu-id="819df-115">**Константа**</span><span class="sxs-lookup"><span data-stu-id="819df-115">**Constant**</span></span>|<span data-ttu-id="819df-116">**Значение**</span><span class="sxs-lookup"><span data-stu-id="819df-116">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="819df-117">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="819df-117">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="819df-118">0x0D000000</span><span class="sxs-lookup"><span data-stu-id="819df-118">0x0D000000</span></span>  <br/> |
|<span data-ttu-id="819df-119">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="819df-119">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="819df-120">0x02000000</span><span class="sxs-lookup"><span data-stu-id="819df-120">0x02000000</span></span>  <br/> |
   
<span data-ttu-id="819df-121">При вызове **IMAPIProp::GetIDsFromNames** укажите следующие значения для структуры **[MAPINAMEID,](mapinameid.md)** на которые указывает параметр *ввода lppPropNames.*</span><span class="sxs-lookup"><span data-stu-id="819df-121">When calling **IMAPIProp::GetIDsFromNames**, specify the following values for the **[MAPINAMEID](mapinameid.md)** structure pointed to by the input parameter  *lppPropNames*  .</span></span> 
  
****

|<span data-ttu-id="819df-122">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="819df-122">**Member**</span></span>|<span data-ttu-id="819df-123">**Значение**</span><span class="sxs-lookup"><span data-stu-id="819df-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="819df-124">lpGuid:</span><span class="sxs-lookup"><span data-stu-id="819df-124">lpGuid:</span></span>  <br/> |<span data-ttu-id="819df-125">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="819df-125">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="819df-126">ulKind:</span><span class="sxs-lookup"><span data-stu-id="819df-126">ulKind:</span></span>  <br/> |<span data-ttu-id="819df-127">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="819df-127">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="819df-128">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="819df-128">Kind.lID:</span></span>  <br/> |<span data-ttu-id="819df-129">dispidCustomFlag</span><span class="sxs-lookup"><span data-stu-id="819df-129">dispidCustomFlag</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="819df-130">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="819df-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="819df-131">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="819df-131">Protocol specifications</span></span>

<span data-ttu-id="819df-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="819df-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="819df-133">Предоставляет определения набора свойств.</span><span class="sxs-lookup"><span data-stu-id="819df-133">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="819df-134">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="819df-134">Header files</span></span>

<span data-ttu-id="819df-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="819df-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="819df-136">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="819df-136">Provides data type definitions.</span></span>
    
<span data-ttu-id="819df-137">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="819df-137">Mapitags.h</span></span>
  
> <span data-ttu-id="819df-138">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="819df-138">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="819df-139">См. также</span><span class="sxs-lookup"><span data-stu-id="819df-139">See also</span></span>



[<span data-ttu-id="819df-140">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="819df-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="819df-141">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="819df-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="819df-142">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="819df-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="819df-143">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="819df-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

