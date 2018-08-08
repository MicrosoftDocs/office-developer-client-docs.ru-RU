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
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810367"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="3339e-103">Каноническое свойство PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3339e-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="3339e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3339e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3339e-105">Указывает, как создать и подсчета значение свойства **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) при изменении свойства имени других контактов.</span><span class="sxs-lookup"><span data-stu-id="3339e-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3339e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="3339e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3339e-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="3339e-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="3339e-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="3339e-108">Property set:</span></span>  <br/> |<span data-ttu-id="3339e-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="3339e-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="3339e-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="3339e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3339e-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="3339e-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="3339e-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="3339e-112">Data type:</span></span>  <br/> |<span data-ttu-id="3339e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3339e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3339e-114">Область:</span><span class="sxs-lookup"><span data-stu-id="3339e-114">Area:</span></span>  <br/> |<span data-ttu-id="3339e-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="3339e-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3339e-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="3339e-116">Remarks</span></span>

<span data-ttu-id="3339e-117">Если это свойство отсутствует или задано значение не описано в следующей таблице или в [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), приложения можно выбрать собственную логику для подсчета значение **dispidFileUnder** как другие изменения свойств имя контакта.</span><span class="sxs-lookup"><span data-stu-id="3339e-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="3339e-118">В следующей таблице, пометка <PropertyName> используется для указания «значение PropertyName».</span><span class="sxs-lookup"><span data-stu-id="3339e-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="3339e-119">Например, если значение свойства **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) — «Егоров», а значение свойства **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) — «Бен», затем "<PidTagGivenName> <PidTagSurname>" указывает строку «Бен Егоров».</span><span class="sxs-lookup"><span data-stu-id="3339e-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="3339e-120">В таблице «\r» указывает, возврат каретки, «\n» указывает символ перевода строки и <space> представляет пробел.</span><span class="sxs-lookup"><span data-stu-id="3339e-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="3339e-121">**Значение свойства **dispidFileUnderId****</span><span class="sxs-lookup"><span data-stu-id="3339e-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="3339e-122">**Описание свойства **dispidFileUnder****</span><span class="sxs-lookup"><span data-stu-id="3339e-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3339e-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3339e-123">0x00000000</span></span>  <br/> |<span data-ttu-id="3339e-124">Пустой PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="3339e-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="3339e-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="3339e-125">0x00003001</span></span>  <br/> |<span data-ttu-id="3339e-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="3339e-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="3339e-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="3339e-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="3339e-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="3339e-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="3339e-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="3339e-133">0x00008017</span></span>  <br/> |<span data-ttu-id="3339e-134">"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="3339e-135">0x00008018</span></span>  <br/> |<span data-ttu-id="3339e-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="3339e-137">0x00008019</span></span>  <br/> |<span data-ttu-id="3339e-138">"\<PidTagSurname\>,\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="3339e-139">0x00008030</span></span>  <br/> |<span data-ttu-id="3339e-140">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="3339e-141">0x00008031</span></span>  <br/> |<span data-ttu-id="3339e-142">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="3339e-143">0x00008032</span></span>  <br/> |<span data-ttu-id="3339e-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="3339e-145">0x00008033</span></span>  <br/> |<span data-ttu-id="3339e-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="3339e-147">0x00008034</span></span>  <br/> |<span data-ttu-id="3339e-148">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="3339e-149">0x00008035</span></span>  <br/> |<span data-ttu-id="3339e-150">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="3339e-151">0x00008036</span></span>  <br/> |<span data-ttu-id="3339e-152">"\<PidTagSurname\>\<пространства\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="3339e-153">0x00008037</span></span>  <br/> |<span data-ttu-id="3339e-154">"\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagSurname\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="3339e-155">0x00008038</span></span>  <br/> |<span data-ttu-id="3339e-156">"\<PidTagSurname\>\<PidTagGivenName\>\<пространства\>\<PidTagMiddleName\>\<пространства\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="3339e-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="3339e-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="3339e-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="3339e-158">Указывает, что при отображении контакт, приложение следует попытаться использовать текущее значение **dispidFileUnder** и другие свойства контакта для поиска «рекомендации» для **dispidFileUnderId** к одному из вышеуказанных значений в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3339e-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="3339e-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="3339e-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="3339e-160">Указывает, что при отображении контакт, приложения выберите соответствующие значения по умолчанию (в соответствии с языковой стандарт) для **dispidFileUnderId** и обновить **dispidFileUnder** в соответствии с выбором.</span><span class="sxs-lookup"><span data-stu-id="3339e-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="3339e-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="3339e-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="3339e-162">**dispidFileUnder** — это PT_UNICODE предоставленного пользователем и не должно изменяться при изменении другого свойства имя контакта.</span><span class="sxs-lookup"><span data-stu-id="3339e-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3339e-163">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="3339e-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3339e-164">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="3339e-164">Protocol specifications</span></span>

<span data-ttu-id="3339e-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3339e-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3339e-166">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3339e-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3339e-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3339e-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3339e-168">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="3339e-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3339e-169">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="3339e-169">Header files</span></span>

<span data-ttu-id="3339e-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3339e-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="3339e-171">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="3339e-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3339e-172">См. также</span><span class="sxs-lookup"><span data-stu-id="3339e-172">See also</span></span>



[<span data-ttu-id="3339e-173">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3339e-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3339e-174">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3339e-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3339e-175">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="3339e-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3339e-176">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="3339e-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

