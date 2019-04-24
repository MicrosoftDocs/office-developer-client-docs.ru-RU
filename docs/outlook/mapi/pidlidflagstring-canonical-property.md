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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357787"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="8b953-103">Каноническое свойство PidLidFlagString</span><span class="sxs-lookup"><span data-stu-id="8b953-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="8b953-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b953-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b953-105">Содержит индекс, идентифицирующий один из набора предварительно определенных текстовых строк, связанных с флагом.</span><span class="sxs-lookup"><span data-stu-id="8b953-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b953-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="8b953-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b953-107">Диспидфлагстринженум</span><span class="sxs-lookup"><span data-stu-id="8b953-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="8b953-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="8b953-108">Property set:</span></span>  <br/> |<span data-ttu-id="8b953-109">Псетид_коммон</span><span class="sxs-lookup"><span data-stu-id="8b953-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="8b953-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="8b953-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8b953-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="8b953-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="8b953-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="8b953-112">Data type:</span></span>  <br/> |<span data-ttu-id="8b953-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8b953-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8b953-114">Область:</span><span class="sxs-lookup"><span data-stu-id="8b953-114">Area:</span></span>  <br/> |<span data-ttu-id="8b953-115">Задача</span><span class="sxs-lookup"><span data-stu-id="8b953-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b953-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b953-116">Remarks</span></span>

<span data-ttu-id="8b953-117">Если это свойство задано, клиенты должны использовать соответствующее строковое значение в приведенных ниже таблицах (например, для замены строки, переведенной на язык текущего пользователя), и игнорировать значение, заданное в **диспидфлагрекуест** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) и **диспидвалидфлагстрингпруф** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8b953-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="8b953-118">Для объектов Contact можно указать следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="8b953-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="8b953-119">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8b953-119">**Value**</span></span>|<span data-ttu-id="8b953-120">**Строка на английском языке**</span><span class="sxs-lookup"><span data-stu-id="8b953-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b953-121">0x00000000 или отсутствует</span><span class="sxs-lookup"><span data-stu-id="8b953-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="8b953-122">Следуйте указаниям, связанным с отображением **диспидфлагрекуест**.</span><span class="sxs-lookup"><span data-stu-id="8b953-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="8b953-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="8b953-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="8b953-124">"К исполнению"</span><span class="sxs-lookup"><span data-stu-id="8b953-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="8b953-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="8b953-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="8b953-126">Вызывать</span><span class="sxs-lookup"><span data-stu-id="8b953-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="8b953-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="8b953-127">0x00000070</span></span>  <br/> |<span data-ttu-id="8b953-128">"Упорядочить собрание"</span><span class="sxs-lookup"><span data-stu-id="8b953-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="8b953-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="8b953-129">0x00000071</span></span>  <br/> |<span data-ttu-id="8b953-130">"Отправить электронную почту"</span><span class="sxs-lookup"><span data-stu-id="8b953-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="8b953-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="8b953-131">0x00000072</span></span>  <br/> |<span data-ttu-id="8b953-132">"Отправить письмо"</span><span class="sxs-lookup"><span data-stu-id="8b953-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="8b953-133">По умолчанию для всех других объектов сообщений предлагается следующее:</span><span class="sxs-lookup"><span data-stu-id="8b953-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="8b953-134">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8b953-134">**Value**</span></span>|<span data-ttu-id="8b953-135">**Строка на английском языке**</span><span class="sxs-lookup"><span data-stu-id="8b953-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b953-136">0x00000000 или отсутствует</span><span class="sxs-lookup"><span data-stu-id="8b953-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="8b953-137">Следуйте указаниям, связанным с отображением **диспидфлагрекуест**.</span><span class="sxs-lookup"><span data-stu-id="8b953-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="8b953-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8b953-138">0x00000001</span></span>  <br/> |<span data-ttu-id="8b953-139">Вызывать</span><span class="sxs-lookup"><span data-stu-id="8b953-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="8b953-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8b953-140">0x00000002</span></span>  <br/> |<span data-ttu-id="8b953-141">"Не переСылать"</span><span class="sxs-lookup"><span data-stu-id="8b953-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="8b953-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="8b953-142">0x00000003</span></span>  <br/> |<span data-ttu-id="8b953-143">"К исполнению"</span><span class="sxs-lookup"><span data-stu-id="8b953-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="8b953-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8b953-144">0x00000004</span></span>  <br/> |<span data-ttu-id="8b953-145">"Для получения сведений"</span><span class="sxs-lookup"><span data-stu-id="8b953-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="8b953-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="8b953-146">0x00000005</span></span>  <br/> |<span data-ttu-id="8b953-147">"Forward" («Переслать»)</span><span class="sxs-lookup"><span data-stu-id="8b953-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="8b953-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="8b953-148">0x00000006</span></span>  <br/> |<span data-ttu-id="8b953-149">"Нет ответа не требуется"</span><span class="sxs-lookup"><span data-stu-id="8b953-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="8b953-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="8b953-150">0x00000007</span></span>  <br/> |<span data-ttu-id="8b953-151">Прочитан</span><span class="sxs-lookup"><span data-stu-id="8b953-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="8b953-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8b953-152">0x00000008</span></span>  <br/> |<span data-ttu-id="8b953-153">"Reply" («Ответить»)</span><span class="sxs-lookup"><span data-stu-id="8b953-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="8b953-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="8b953-154">0x00000009</span></span>  <br/> |<span data-ttu-id="8b953-155">"Ответить всем"</span><span class="sxs-lookup"><span data-stu-id="8b953-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="8b953-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="8b953-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="8b953-157">Смотрите</span><span class="sxs-lookup"><span data-stu-id="8b953-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="8b953-158">Все указанные выше строки можно перевести на язык пользователя, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="8b953-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8b953-159">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="8b953-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b953-160">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="8b953-160">Protocol specifications</span></span>

<span data-ttu-id="8b953-161">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b953-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b953-162">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8b953-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8b953-163">[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b953-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b953-164">Задает свойства и операции, связанные с пометкой.</span><span class="sxs-lookup"><span data-stu-id="8b953-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b953-165">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="8b953-165">Header files</span></span>

<span data-ttu-id="8b953-166">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="8b953-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b953-167">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="8b953-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b953-168">См. также</span><span class="sxs-lookup"><span data-stu-id="8b953-168">See also</span></span>



[<span data-ttu-id="8b953-169">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="8b953-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b953-170">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="8b953-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b953-171">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="8b953-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b953-172">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="8b953-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

