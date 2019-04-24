---
title: Каноническое свойство PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355708"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="d85ba-103">Каноническое свойство PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="d85ba-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="d85ba-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85ba-105">Указывает, как создать и повторно вычислить значение свойства **диспидфилеундер** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) при изменении других свойств имени контакта.</span><span class="sxs-lookup"><span data-stu-id="d85ba-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d85ba-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d85ba-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d85ba-107">Диспидфилеундерид</span><span class="sxs-lookup"><span data-stu-id="d85ba-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="d85ba-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="d85ba-108">Property set:</span></span>  <br/> |<span data-ttu-id="d85ba-109">Псетид_аддресс</span><span class="sxs-lookup"><span data-stu-id="d85ba-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="d85ba-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="d85ba-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d85ba-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="d85ba-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="d85ba-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d85ba-112">Data type:</span></span>  <br/> |<span data-ttu-id="d85ba-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d85ba-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d85ba-114">Область:</span><span class="sxs-lookup"><span data-stu-id="d85ba-114">Area:</span></span>  <br/> |<span data-ttu-id="d85ba-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="d85ba-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d85ba-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d85ba-116">Remarks</span></span>

<span data-ttu-id="d85ba-117">Если это свойство отсутствует или для него задано значение, не подробное в таблице ниже или в [[MS-оксокнтк]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), приложение может выбрать собственную логику для повторного вычисления значения **диспидфилеундер** в качестве другого свойства имени контакта.</span><span class="sxs-lookup"><span data-stu-id="d85ba-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="d85ba-118">В следующей таблице приведена нотация <PropertyName> , в которой указывается значение PropertyName.</span><span class="sxs-lookup"><span data-stu-id="d85ba-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="d85ba-119">Например, если значение свойства **пр_сурнаме** ([PidTagSurname](pidtagsurname-canonical-property.md)) — "Smith", а значение свойства **пр_гивен_наме** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — "Бен", то "<PidTagGivenName> <PidTagSurname>" указывает строку "Бен Smith".</span><span class="sxs-lookup"><span data-stu-id="d85ba-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="d85ba-120">В таблице "\r" указывает символ возврата каретки, "\n" определяет символ перевода строки и <space> представляет символ пробела.</span><span class="sxs-lookup"><span data-stu-id="d85ba-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="d85ba-121">\*\*Значение свойства \*\*диспидфилеундерид\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d85ba-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="d85ba-122">\*\*Описание свойства \*\*диспидфилеундер\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d85ba-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d85ba-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d85ba-123">0x00000000</span></span>  <br/> |<span data-ttu-id="d85ba-124">Пустой ПТ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="d85ba-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="d85ba-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="d85ba-125">0x00003001</span></span>  <br/> |<span data-ttu-id="d85ba-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="d85ba-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="d85ba-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="d85ba-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="d85ba-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="d85ba-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="d85ba-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="d85ba-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="d85ba-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="d85ba-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="d85ba-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="d85ba-133">0x00008017</span></span>  <br/> |<span data-ttu-id="d85ba-134">"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="d85ba-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="d85ba-135">0x00008018</span></span>  <br/> |<span data-ttu-id="d85ba-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="d85ba-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="d85ba-137">0x00008019</span></span>  <br/> |<span data-ttu-id="d85ba-138">"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\>Space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="d85ba-139">0x00008030</span></span>  <br/> |<span data-ttu-id="d85ba-140">"\<PidTagSurname\>\<\>PidTagGivenName\<Space\>PidTagMiddleName\>"\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="d85ba-141">0x00008031</span></span>  <br/> |<span data-ttu-id="d85ba-142">"\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>PidTagMiddleName\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="d85ba-143">0x00008032</span></span>  <br/> |<span data-ttu-id="d85ba-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="d85ba-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="d85ba-145">0x00008033</span></span>  <br/> |<span data-ttu-id="d85ba-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>PidTagMiddleName\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="d85ba-147">0x00008034</span></span>  <br/> |<span data-ttu-id="d85ba-148">"\<PidTagSurname\>\<PidTagGivenName\>\>Space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="d85ba-149">0x00008035</span></span>  <br/> |<span data-ttu-id="d85ba-150">"\<PidTagSurname\>\<Space\>\<\>PidTagGivenName Space\>PidTagMiddleName \r\n PidTagCompanyName"\<\>\<\>\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="d85ba-151">0x00008036</span></span>  <br/> |<span data-ttu-id="d85ba-152">"\<PidTagSurname\>\<Space\>\>\>PidTagGivenName\>Space PidTagMiddleName\>Space\>PidTagGeneration\<"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="d85ba-153">0x00008037</span></span>  <br/> |<span data-ttu-id="d85ba-154">"\<PidTagGivenName\>\<Space\>\>\>PidTagMiddleName\>Space PidTagSurname\>Space\>PidTagGeneration\<"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="d85ba-155">0x00008038</span></span>  <br/> |<span data-ttu-id="d85ba-156">"\<PidTagSurname\>\<PidTagGivenName\>\>Space\>PidTagMiddleName\>Space\>PidTagGeneration"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="d85ba-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="d85ba-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="d85ba-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="d85ba-158">Указывает, что при отображении контакта приложение должно попытаться использовать текущее значение **диспидфилеундер** и другие свойства контакта, чтобы найти "наилучшее значение" для **диспидфилеундерид** к одному из предыдущих значений в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="d85ba-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="d85ba-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="d85ba-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="d85ba-160">Указывает, что при отображении контакта приложение должно выбрать соответствующие значения по умолчанию (в соответствии с языковым стандартом языка) для **диспидфилеундерид** и обновить **диспидфилеундер** в соответствии с выбором.</span><span class="sxs-lookup"><span data-stu-id="d85ba-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="d85ba-161">равен</span><span class="sxs-lookup"><span data-stu-id="d85ba-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="d85ba-162">**диспидфилеундер** — это предоставленный пользователем пт_уникоде, и его не следует изменять при изменении другого свойства имени контакта.</span><span class="sxs-lookup"><span data-stu-id="d85ba-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d85ba-163">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d85ba-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d85ba-164">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="d85ba-164">Protocol specifications</span></span>

<span data-ttu-id="d85ba-165">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d85ba-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d85ba-166">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d85ba-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d85ba-167">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d85ba-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d85ba-168">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="d85ba-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d85ba-169">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="d85ba-169">Header files</span></span>

<span data-ttu-id="d85ba-170">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d85ba-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="d85ba-171">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d85ba-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d85ba-172">См. также</span><span class="sxs-lookup"><span data-stu-id="d85ba-172">See also</span></span>



[<span data-ttu-id="d85ba-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ba-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d85ba-174">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ba-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d85ba-175">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d85ba-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d85ba-176">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d85ba-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

