---
title: Каноническое свойство PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342674"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="6c180-103">Каноническое свойство PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="6c180-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="6c180-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c180-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c180-105">Содержит битовую маску параметров кодирования.</span><span class="sxs-lookup"><span data-stu-id="6c180-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c180-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6c180-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c180-107">ПР_СЕНД_ИНТЕРНЕТ_ЕНКОДИНГ</span><span class="sxs-lookup"><span data-stu-id="6c180-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="6c180-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6c180-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c180-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="6c180-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="6c180-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6c180-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c180-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6c180-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6c180-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6c180-112">Area:</span></span>  <br/> |<span data-ttu-id="6c180-113">Address</span><span class="sxs-lookup"><span data-stu-id="6c180-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c180-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c180-114">Remarks</span></span>

<span data-ttu-id="6c180-115">Задайте это свойство, чтобы указать используемые параметры кодировки.</span><span class="sxs-lookup"><span data-stu-id="6c180-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="6c180-116">Данное свойство содержит следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="6c180-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="6c180-117">БОДИ_ЕНКОДИНГ_ХТМЛ</span><span class="sxs-lookup"><span data-stu-id="6c180-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="6c180-118">Кодирует текст сообщения в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="6c180-118">Encode the message text in HTML.</span></span> <span data-ttu-id="6c180-119">Этот флаг игнорируется, если не установлен флаг ЕНКОДИНГ_МИМЕ.</span><span class="sxs-lookup"><span data-stu-id="6c180-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6c180-120">БОДИ_ЕНКОДИНГ_ТЕКСТ_АНД_ХТМЛ</span><span class="sxs-lookup"><span data-stu-id="6c180-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="6c180-121">Кодирование текста сообщения с помощью текстовых и HTML-файлов в виде многоцелевого альтернативного расширения почты в Интернете (MIME).</span><span class="sxs-lookup"><span data-stu-id="6c180-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="6c180-122">Этот флаг игнорируется, если не установлен флаг ЕНКОДИНГ_МИМЕ.</span><span class="sxs-lookup"><span data-stu-id="6c180-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6c180-123">ЕНКОДИНГ_МИМЕ</span><span class="sxs-lookup"><span data-stu-id="6c180-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="6c180-124">Кодирование сообщения с использованием MIME.</span><span class="sxs-lookup"><span data-stu-id="6c180-124">Encode the message using MIME.</span></span> <span data-ttu-id="6c180-125">Если этот флаг не установлен, MAPI кодирует текст сообщения в виде обычного текста и вложений в КОДИРОВКе UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="6c180-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="6c180-126">ЕНКОДИНГ_ПРЕФЕРЕНЦЕ</span><span class="sxs-lookup"><span data-stu-id="6c180-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="6c180-127">Используйте другие флаги в этой битовой маске, чтобы определить кодировку.</span><span class="sxs-lookup"><span data-stu-id="6c180-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="6c180-128">Если этот флаг не установлен, MAPI оставляет его в системе обмена сообщениями, чтобы принимать решения по кодированию.</span><span class="sxs-lookup"><span data-stu-id="6c180-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="6c180-129">МАК_АТТАЧ_ЕНКОДИНГ_АППЛЕДАУБЛЕ</span><span class="sxs-lookup"><span data-stu-id="6c180-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="6c180-130">Кодирование вложений Macintosh в двойном режиме Apple.</span><span class="sxs-lookup"><span data-stu-id="6c180-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="6c180-131">Этот флаг игнорируется, если не установлен флаг ЕНКОДИНГ_МИМЕ.</span><span class="sxs-lookup"><span data-stu-id="6c180-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6c180-132">МАК_АТТАЧ_ЕНКОДИНГ_АППЛЕСИНГЛЕ</span><span class="sxs-lookup"><span data-stu-id="6c180-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="6c180-133">Кодирование вложений Macintosh в Apple Single Mode.</span><span class="sxs-lookup"><span data-stu-id="6c180-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="6c180-134">Этот флаг игнорируется, если не установлен флаг ЕНКОДИНГ_МИМЕ.</span><span class="sxs-lookup"><span data-stu-id="6c180-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="6c180-135">МАК_АТТАЧ_ЕНКОДИНГ_УУЕНКОДЕ</span><span class="sxs-lookup"><span data-stu-id="6c180-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="6c180-136">Кодирование вложений Macintosh в КОДИРОВКе UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="6c180-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="6c180-137">Если установлен флаг ЕНКОДИНГ_МИМЕ, этот флаг игнорируется, а вместо этого используется кодировка BinHex.</span><span class="sxs-lookup"><span data-stu-id="6c180-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="6c180-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6c180-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c180-139">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6c180-139">Protocol specifications</span></span>

<span data-ttu-id="6c180-140">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c180-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c180-141">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6c180-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c180-142">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c180-142">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c180-143">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c180-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="6c180-144">[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c180-144">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c180-145">Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c180-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="6c180-146">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c180-146">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c180-147">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="6c180-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6c180-148">[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c180-148">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c180-149">Задает свойства и операции, допустимые для объектов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6c180-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c180-150">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="6c180-150">Header files</span></span>

<span data-ttu-id="6c180-151">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="6c180-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c180-152">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6c180-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c180-153">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="6c180-153">Mapitags.h</span></span>
  
> <span data-ttu-id="6c180-154">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="6c180-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c180-155">См. также</span><span class="sxs-lookup"><span data-stu-id="6c180-155">See also</span></span>



[<span data-ttu-id="6c180-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6c180-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c180-157">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="6c180-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c180-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6c180-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c180-159">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6c180-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

