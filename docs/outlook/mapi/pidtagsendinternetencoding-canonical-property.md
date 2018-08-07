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
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811892"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a><span data-ttu-id="2318e-103">Каноническое свойство PidTagSendInternetEncoding</span><span class="sxs-lookup"><span data-stu-id="2318e-103">PidTagSendInternetEncoding Canonical Property</span></span>

  
  
<span data-ttu-id="2318e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2318e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2318e-105">Содержит Битовая маска установки кодировки.</span><span class="sxs-lookup"><span data-stu-id="2318e-105">Contains a bitmask of encoding preferences.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2318e-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="2318e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2318e-107">PR_SEND_INTERNET_ENCODING</span><span class="sxs-lookup"><span data-stu-id="2318e-107">PR_SEND_INTERNET_ENCODING</span></span>  <br/> |
|<span data-ttu-id="2318e-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="2318e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2318e-109">0x3A71</span><span class="sxs-lookup"><span data-stu-id="2318e-109">0x3A71</span></span>  <br/> |
|<span data-ttu-id="2318e-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="2318e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2318e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2318e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2318e-112">Область:</span><span class="sxs-lookup"><span data-stu-id="2318e-112">Area:</span></span>  <br/> |<span data-ttu-id="2318e-113">Address</span><span class="sxs-lookup"><span data-stu-id="2318e-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2318e-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2318e-114">Remarks</span></span>

<span data-ttu-id="2318e-115">Задайте это свойство, чтобы указать параметры кодирования используется.</span><span class="sxs-lookup"><span data-stu-id="2318e-115">Set this property to indicate the encoding options used.</span></span> 
  
<span data-ttu-id="2318e-116">Это свойство содержит следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2318e-116">This property contains the following flags:</span></span>
  
<span data-ttu-id="2318e-117">BODY_ENCODING_HTML</span><span class="sxs-lookup"><span data-stu-id="2318e-117">BODY_ENCODING_HTML</span></span> 
  
> <span data-ttu-id="2318e-118">Шифрование текста сообщения в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="2318e-118">Encode the message text in HTML.</span></span> <span data-ttu-id="2318e-119">Этот флаг игнорируется, если не задан флаг ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="2318e-119">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="2318e-120">BODY_ENCODING_TEXT_AND_HTML</span><span class="sxs-lookup"><span data-stu-id="2318e-120">BODY_ENCODING_TEXT_AND_HTML</span></span> 
  
> <span data-ttu-id="2318e-121">Шифрование текста сообщения, используя текст и HTML-код в качестве альтернативы многокомпонентных Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="2318e-121">Encode the message text using text and HTML as Multipurpose Internet Mail Extensions (MIME) multipart alternatives.</span></span> <span data-ttu-id="2318e-122">Этот флаг игнорируется, если не задан флаг ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="2318e-122">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="2318e-123">ENCODING_MIME</span><span class="sxs-lookup"><span data-stu-id="2318e-123">ENCODING_MIME</span></span> 
  
> <span data-ttu-id="2318e-124">Кодировки сообщений с помощью MIME.</span><span class="sxs-lookup"><span data-stu-id="2318e-124">Encode the message using MIME.</span></span> <span data-ttu-id="2318e-125">Если этот флаг не установлен, MAPI кодировка текста сообщения в виде обычного текста и вложений в UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="2318e-125">If this flag is not set, MAPI encodes the message text in plain text and the attachments in UUENCODE.</span></span> 
    
<span data-ttu-id="2318e-126">ENCODING_PREFERENCE</span><span class="sxs-lookup"><span data-stu-id="2318e-126">ENCODING_PREFERENCE</span></span> 
  
> <span data-ttu-id="2318e-127">Используйте другие флаги в этом Битовая маска для определения кодировки.</span><span class="sxs-lookup"><span data-stu-id="2318e-127">Use the other flags in this bitmask to determine the encoding.</span></span> <span data-ttu-id="2318e-128">Если этот флаг не установлен, MAPI оставляет его в систему обмена сообщениями для принятия решений кодировки.</span><span class="sxs-lookup"><span data-stu-id="2318e-128">If this flag is not set, MAPI leaves it to the messaging system to make encoding decisions.</span></span> 
    
<span data-ttu-id="2318e-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span><span class="sxs-lookup"><span data-stu-id="2318e-129">MAC_ATTACH_ENCODING_APPLEDOUBLE</span></span> 
  
> <span data-ttu-id="2318e-130">Кодирование вложений Macintosh в режиме двойного Apple.</span><span class="sxs-lookup"><span data-stu-id="2318e-130">Encode Macintosh attachments in Apple double mode.</span></span> <span data-ttu-id="2318e-131">Этот флаг игнорируется, если не задан флаг ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="2318e-131">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="2318e-132">MAC_ATTACH_ENCODING_APPLESINGLE</span><span class="sxs-lookup"><span data-stu-id="2318e-132">MAC_ATTACH_ENCODING_APPLESINGLE</span></span> 
  
> <span data-ttu-id="2318e-133">Кодирование вложений Macintosh в одном режиме Apple.</span><span class="sxs-lookup"><span data-stu-id="2318e-133">Encode Macintosh attachments in Apple single mode.</span></span> <span data-ttu-id="2318e-134">Этот флаг игнорируется, если не задан флаг ENCODING_MIME.</span><span class="sxs-lookup"><span data-stu-id="2318e-134">This flag is ignored unless the ENCODING_MIME flag is set.</span></span> 
    
<span data-ttu-id="2318e-135">MAC_ATTACH_ENCODING_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="2318e-135">MAC_ATTACH_ENCODING_UUENCODE</span></span> 
  
> <span data-ttu-id="2318e-136">Кодирование вложений Macintosh в UUENCODE.</span><span class="sxs-lookup"><span data-stu-id="2318e-136">Encode Macintosh attachments in UUENCODE.</span></span> <span data-ttu-id="2318e-137">Если значение флага ENCODING_MIME, этот флаг игнорируется и кодировки BinHex используется вместо этого.</span><span class="sxs-lookup"><span data-stu-id="2318e-137">If the ENCODING_MIME flag is set, this flag is ignored and BinHex encoding is used instead.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="2318e-138">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="2318e-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2318e-139">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="2318e-139">Protocol specifications</span></span>

<span data-ttu-id="2318e-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2318e-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2318e-141">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2318e-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2318e-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2318e-142">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2318e-143">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2318e-143">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="2318e-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2318e-144">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2318e-145">Преобразование conventions стандартных электронной почты Интернета объекты сообщений.</span><span class="sxs-lookup"><span data-stu-id="2318e-145">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="2318e-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2318e-146">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2318e-147">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="2318e-147">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="2318e-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2318e-148">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2318e-149">Задает свойства и операции, допустимые для объектов сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="2318e-149">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2318e-150">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="2318e-150">Header files</span></span>

<span data-ttu-id="2318e-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2318e-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="2318e-152">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="2318e-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="2318e-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2318e-153">Mapitags.h</span></span>
  
> <span data-ttu-id="2318e-154">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2318e-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2318e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="2318e-155">See also</span></span>



[<span data-ttu-id="2318e-156">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2318e-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2318e-157">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2318e-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2318e-158">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="2318e-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2318e-159">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="2318e-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

