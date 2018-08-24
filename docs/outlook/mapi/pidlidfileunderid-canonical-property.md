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
ms.openlocfilehash: 0a4fdb94877fb9491005fc650c206ffefd3f8b94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578418"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="00b63-103">Каноническое свойство PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="00b63-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="00b63-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00b63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00b63-105">Указывает, как создать и подсчета значение свойства **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) при изменении свойства имени других контактов.</span><span class="sxs-lookup"><span data-stu-id="00b63-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00b63-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="00b63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00b63-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="00b63-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="00b63-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="00b63-108">Property set:</span></span>  <br/> |<span data-ttu-id="00b63-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="00b63-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="00b63-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="00b63-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00b63-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="00b63-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="00b63-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="00b63-112">Data type:</span></span>  <br/> |<span data-ttu-id="00b63-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00b63-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00b63-114">Область:</span><span class="sxs-lookup"><span data-stu-id="00b63-114">Area:</span></span>  <br/> |<span data-ttu-id="00b63-115">Contact</span><span class="sxs-lookup"><span data-stu-id="00b63-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00b63-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="00b63-116">Remarks</span></span>

<span data-ttu-id="00b63-117">Если это свойство отсутствует или задано значение не описано в следующей таблице или в [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), приложения можно выбрать собственную логику для подсчета значение **dispidFileUnder** как другие изменения свойств имя контакта.</span><span class="sxs-lookup"><span data-stu-id="00b63-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="00b63-118">В следующей таблице, пометка <PropertyName> используется для указания «значение PropertyName».</span><span class="sxs-lookup"><span data-stu-id="00b63-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="00b63-119">Например, если значение свойства **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) — «Егоров», а значение свойства **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — «Бен», затем "<PidTagGivenName> <PidTagSurname>" указывает строку «Бен Егоров».</span><span class="sxs-lookup"><span data-stu-id="00b63-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="00b63-120">В таблице «\r» указывает, возврат каретки, «\n» указывает символ перевода строки и <space> представляет пробел.</span><span class="sxs-lookup"><span data-stu-id="00b63-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="00b63-121">**Значение свойства **dispidFileUnderId****</span><span class="sxs-lookup"><span data-stu-id="00b63-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="00b63-122">**Описание свойства **dispidFileUnder****</span><span class="sxs-lookup"><span data-stu-id="00b63-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00b63-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00b63-123">0x00000000</span></span>  <br/> |<span data-ttu-id="00b63-124">Пустой PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="00b63-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="00b63-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="00b63-125">0x00003001</span></span>  <br/> |<span data-ttu-id="00b63-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="00b63-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="00b63-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="00b63-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="00b63-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="00b63-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="00b63-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="00b63-133">0x00008017</span></span>  <br/> |<span data-ttu-id="00b63-134">"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="00b63-135">0x00008018</span></span>  <br/> |<span data-ttu-id="00b63-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="00b63-137">0x00008019</span></span>  <br/> |<span data-ttu-id="00b63-138">"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="00b63-139">0x00008030</span></span>  <br/> |<span data-ttu-id="00b63-140">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="00b63-141">0x00008031</span></span>  <br/> |<span data-ttu-id="00b63-142">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="00b63-143">0x00008032</span></span>  <br/> |<span data-ttu-id="00b63-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="00b63-145">0x00008033</span></span>  <br/> |<span data-ttu-id="00b63-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="00b63-147">0x00008034</span></span>  <br/> |<span data-ttu-id="00b63-148">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="00b63-149">0x00008035</span></span>  <br/> |<span data-ttu-id="00b63-150">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="00b63-151">0x00008036</span></span>  <br/> |<span data-ttu-id="00b63-152">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="00b63-153">0x00008037</span></span>  <br/> |<span data-ttu-id="00b63-154">"\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagSurname\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="00b63-155">0x00008038</span></span>  <br/> |<span data-ttu-id="00b63-156">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="00b63-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00b63-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="00b63-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="00b63-158">Указывает, что при отображении контакт, приложение следует попытаться использовать текущее значение **dispidFileUnder** и другие свойства контакта для поиска «рекомендации» для **dispidFileUnderId** к одному из вышеуказанных значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="00b63-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="00b63-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="00b63-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="00b63-160">Указывает, что при отображении контакт, приложения выберите соответствующие значения по умолчанию (в соответствии с языковой стандарт) для **dispidFileUnderId** и обновить **dispidFileUnder** в соответствии с выбором.</span><span class="sxs-lookup"><span data-stu-id="00b63-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="00b63-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="00b63-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="00b63-162">**dispidFileUnder** — это PT_UNICODE предоставленного пользователем и не должно изменяться при изменении другого свойства имя контакта.</span><span class="sxs-lookup"><span data-stu-id="00b63-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00b63-163">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="00b63-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00b63-164">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="00b63-164">Protocol specifications</span></span>

<span data-ttu-id="00b63-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00b63-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00b63-166">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="00b63-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00b63-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00b63-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00b63-168">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="00b63-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00b63-169">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="00b63-169">Header files</span></span>

<span data-ttu-id="00b63-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00b63-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="00b63-171">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="00b63-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00b63-172">См. также</span><span class="sxs-lookup"><span data-stu-id="00b63-172">See also</span></span>



[<span data-ttu-id="00b63-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00b63-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00b63-174">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="00b63-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00b63-175">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="00b63-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00b63-176">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="00b63-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

