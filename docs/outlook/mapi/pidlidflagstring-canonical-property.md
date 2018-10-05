---
title: Каноническое свойство PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395583"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="33fb9-103">Каноническое свойство PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="33fb9-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="33fb9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33fb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33fb9-105">Содержит индекс, который определяет одну из набора предварительно определенных текстовых строк, связанных с флагом.</span><span class="sxs-lookup"><span data-stu-id="33fb9-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33fb9-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="33fb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33fb9-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="33fb9-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="33fb9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="33fb9-108">Property set:</span></span>  <br/> |<span data-ttu-id="33fb9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="33fb9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="33fb9-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="33fb9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="33fb9-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="33fb9-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="33fb9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="33fb9-112">Data type:</span></span>  <br/> |<span data-ttu-id="33fb9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33fb9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33fb9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="33fb9-114">Area:</span></span>  <br/> |<span data-ttu-id="33fb9-115">Task</span><span class="sxs-lookup"><span data-stu-id="33fb9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33fb9-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="33fb9-116">Remarks</span></span>

<span data-ttu-id="33fb9-117">Если задано это свойство, клиенты должны использовать соответствующее значение строки в таблице ниже (например, чтобы заменить строку, переведенный на язык текущего пользователя), а следует игнорировать значение, установленное в **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) и **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33fb9-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="33fb9-118">Доступны следующие параметры по умолчанию, предложенных пользователя для контактных объектов:</span><span class="sxs-lookup"><span data-stu-id="33fb9-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="33fb9-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="33fb9-119">**Value**</span></span>|<span data-ttu-id="33fb9-120">**Строка на английском языке**</span><span class="sxs-lookup"><span data-stu-id="33fb9-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33fb9-121">0x00000000 или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="33fb9-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="33fb9-122">Следуйте указаниям, связанные с отображением **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="33fb9-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="33fb9-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="33fb9-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="33fb9-124">«Исполнению»</span><span class="sxs-lookup"><span data-stu-id="33fb9-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="33fb9-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="33fb9-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="33fb9-126">«Звонок»</span><span class="sxs-lookup"><span data-stu-id="33fb9-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="33fb9-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="33fb9-127">0x00000070</span></span>  <br/> |<span data-ttu-id="33fb9-128">«Упорядочить собрания»</span><span class="sxs-lookup"><span data-stu-id="33fb9-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="33fb9-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="33fb9-129">0x00000071</span></span>  <br/> |<span data-ttu-id="33fb9-130">«Отправка электронной почты»</span><span class="sxs-lookup"><span data-stu-id="33fb9-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="33fb9-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="33fb9-131">0x00000072</span></span>  <br/> |<span data-ttu-id="33fb9-132">«Отправлять письма»</span><span class="sxs-lookup"><span data-stu-id="33fb9-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="33fb9-133">Доступны следующие параметры по умолчанию, предложенных пользователей для всех других объектов сообщения:</span><span class="sxs-lookup"><span data-stu-id="33fb9-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="33fb9-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="33fb9-134">**Value**</span></span>|<span data-ttu-id="33fb9-135">**Строка на английском языке**</span><span class="sxs-lookup"><span data-stu-id="33fb9-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="33fb9-136">0x00000000 или отсутствует.</span><span class="sxs-lookup"><span data-stu-id="33fb9-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="33fb9-137">Следуйте указаниям, связанные с отображением **dispidFlagRequest**.</span><span class="sxs-lookup"><span data-stu-id="33fb9-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="33fb9-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="33fb9-138">0x00000001</span></span>  <br/> |<span data-ttu-id="33fb9-139">«Звонок»</span><span class="sxs-lookup"><span data-stu-id="33fb9-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="33fb9-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="33fb9-140">0x00000002</span></span>  <br/> |<span data-ttu-id="33fb9-141">«Не пересылать»</span><span class="sxs-lookup"><span data-stu-id="33fb9-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="33fb9-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="33fb9-142">0x00000003</span></span>  <br/> |<span data-ttu-id="33fb9-143">«Исполнению»</span><span class="sxs-lookup"><span data-stu-id="33fb9-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="33fb9-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="33fb9-144">0x00000004</span></span>  <br/> |<span data-ttu-id="33fb9-145">«К Вашему сведению»</span><span class="sxs-lookup"><span data-stu-id="33fb9-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="33fb9-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="33fb9-146">0x00000005</span></span>  <br/> |<span data-ttu-id="33fb9-147">«Вперед»</span><span class="sxs-lookup"><span data-stu-id="33fb9-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="33fb9-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="33fb9-148">0x00000006</span></span>  <br/> |<span data-ttu-id="33fb9-149">«Ответа не требуется»</span><span class="sxs-lookup"><span data-stu-id="33fb9-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="33fb9-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="33fb9-150">0x00000007</span></span>  <br/> |<span data-ttu-id="33fb9-151">«Чтение»</span><span class="sxs-lookup"><span data-stu-id="33fb9-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="33fb9-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="33fb9-152">0x00000008</span></span>  <br/> |<span data-ttu-id="33fb9-153">«Ответ»</span><span class="sxs-lookup"><span data-stu-id="33fb9-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="33fb9-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="33fb9-154">0x00000009</span></span>  <br/> |<span data-ttu-id="33fb9-155">«Ответить всем»</span><span class="sxs-lookup"><span data-stu-id="33fb9-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="33fb9-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="33fb9-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="33fb9-157">«Обзор»</span><span class="sxs-lookup"><span data-stu-id="33fb9-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="33fb9-158">Все строки, указанных выше может быть переведено на язык пользователя при необходимости.</span><span class="sxs-lookup"><span data-stu-id="33fb9-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="33fb9-159">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="33fb9-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="33fb9-160">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="33fb9-160">Protocol specifications</span></span>

<span data-ttu-id="33fb9-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33fb9-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33fb9-162">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="33fb9-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="33fb9-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="33fb9-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="33fb9-164">Задает свойства и операции, связанные с флагов.</span><span class="sxs-lookup"><span data-stu-id="33fb9-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="33fb9-165">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="33fb9-165">Header files</span></span>

<span data-ttu-id="33fb9-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33fb9-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="33fb9-167">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="33fb9-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33fb9-168">См. также</span><span class="sxs-lookup"><span data-stu-id="33fb9-168">See also</span></span>



[<span data-ttu-id="33fb9-169">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33fb9-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33fb9-170">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="33fb9-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33fb9-171">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="33fb9-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33fb9-172">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="33fb9-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

