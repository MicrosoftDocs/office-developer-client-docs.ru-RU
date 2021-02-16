---
title: Вложенные файлы и сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436841"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="90103-103">Вложенные файлы и сообщения</span><span class="sxs-lookup"><span data-stu-id="90103-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="90103-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90103-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90103-105">Если MIME с TNEF используется при кодивной кодивности содержимого сообщения, все свойства и содержимое вложений находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="90103-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="90103-106">Сам TNEF — это один двоичный вложенный файл с именем Winmail.dat, закодированный как описано для MIME без TNEF.</span><span class="sxs-lookup"><span data-stu-id="90103-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="90103-107">Если MIME используется без TNEF, вложенные файлы отправляются в качестве частей содержимого сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="90103-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="90103-108">Имя файла помещается в параметр  *name*  в заглавную папку типа  *content*  для вложения.</span><span class="sxs-lookup"><span data-stu-id="90103-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="90103-109">Набор символов для вложения помещается в параметр  *charset*  для типа  *Content;*  оно и кодировидная передача содержимого определяются путем сканирования всего содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="90103-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="90103-110">Вложения URL-адресов обрабатываются особым образом:</span><span class="sxs-lookup"><span data-stu-id="90103-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="90103-111">Если вложение является URL-адресом (вложенный файл с расширением. URL-адрес), а режим доступа, определенный в нем, анонимный FTP, кодируется как внешнее сообщение, а содержимое файла (URL-адрес) копируется в загон внешнего сообщения.</span><span class="sxs-lookup"><span data-stu-id="90103-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="90103-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span><span class="sxs-lookup"><span data-stu-id="90103-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="90103-113">Если найдены только 7-битные символы и длина строки не превышает 140 символов, вложением будет текст ASCII.</span><span class="sxs-lookup"><span data-stu-id="90103-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="90103-114">*Тип контента: текст/обычный; charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="90103-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="90103-115">Если найдены длинные строки или до 25 % 8-битных символов, содержимое вложения — это текст, а набор символов определяется региональными настройками.</span><span class="sxs-lookup"><span data-stu-id="90103-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="90103-116">Его следует выбирать из наборов символов, определенных стандартом ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="90103-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="90103-117">*Тип контента: text/plain; charset=ISO-8859-1*  (например)</span><span class="sxs-lookup"><span data-stu-id="90103-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="90103-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="90103-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="90103-119">Если для 25% или более символов установлен высокий бит, вложение будет двоичным.</span><span class="sxs-lookup"><span data-stu-id="90103-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="90103-120">Кодируются с помощью алгоритма Base64.</span><span class="sxs-lookup"><span data-stu-id="90103-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="90103-121">*Тип контента: application/octet-stream*  (по умолчанию на основе расширения файла)</span><span class="sxs-lookup"><span data-stu-id="90103-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="90103-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="90103-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="90103-123">В исходящие сообщения тип контента должен быть производным от трехбуквеченного расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="90103-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="90103-124">Это сопоставление существует в системный реестр; под строкой с именем "Content Type" (Тип контента), которая предоставляет тип контента MIME, если он определен.</span><span class="sxs-lookup"><span data-stu-id="90103-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="90103-125">Этот пример для TIFF-файла изображения:</span><span class="sxs-lookup"><span data-stu-id="90103-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="90103-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="90103-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="90103-127">Программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="90103-127">Software</span></span>\
  
<span data-ttu-id="90103-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="90103-128">Microsoft</span></span>\
  
<span data-ttu-id="90103-129">Classes</span><span class="sxs-lookup"><span data-stu-id="90103-129">Classes</span></span>\
  
<span data-ttu-id="90103-130">.tif</span><span class="sxs-lookup"><span data-stu-id="90103-130">.tif</span></span>
  
<span data-ttu-id="90103-131">Тип контента = "image/tiff"</span><span class="sxs-lookup"><span data-stu-id="90103-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="90103-132">Если сопоставление для расширения файла не существует, следует использовать поток  *приложения или октета*  по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90103-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="90103-133">Во входящие сообщения тип контента для вложения всегда следует копировать в свойство MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag).](pidtagattachmimetag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="90103-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="90103-134">Даже если для вложенного файла определено имя файла, расширение, соотносимые с типом контента, следует использовать в свойствах **PR_ATTACH_FILENAME** ([PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)и **PR_ATTACH_EXTENSION** ([PidTagAttachExtension).](pidtagattachextension-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="90103-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="90103-135">Параметр  *name*  официально не задан в RFC 821.</span><span class="sxs-lookup"><span data-stu-id="90103-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="90103-136">По мере развития стандартов Корпорация Майкрософт рассмотрит возможность указания альтернативного сопоставления для вложенных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="90103-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="90103-137">Исходящие вложенные сообщения отправляются как \* Content-type: message/rfc822 \* Messages within attached messages are encoded recursively, in their proper place.</span><span class="sxs-lookup"><span data-stu-id="90103-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="90103-138">Части содержимого входящие сообщений  *с content-Type: multipart/digest*  также со картой внедренных сообщений.</span><span class="sxs-lookup"><span data-stu-id="90103-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="90103-139">Если uuencode с TNEF используется при кодировании содержимого сообщения, все свойства и содержимое вложения находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="90103-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="90103-140">Сам TNEF — это один двоичный вложенный файл с именем Winmail.dat, закодированный как описано для Uuencode без TNEF.</span><span class="sxs-lookup"><span data-stu-id="90103-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="90103-141">Если uuencode используется без TNEF, все вложенные файлы обрабатываются как двоичные и uuencoded, следуя тексту сообщения.</span><span class="sxs-lookup"><span data-stu-id="90103-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="90103-142">Имя файла присутствует в загоделе uuencode:</span><span class="sxs-lookup"><span data-stu-id="90103-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="90103-143">0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="90103-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="90103-144">... data ...</span><span class="sxs-lookup"><span data-stu-id="90103-144">... data ...</span></span> 
  
 <span data-ttu-id="90103-145">end</span><span class="sxs-lookup"><span data-stu-id="90103-145">end</span></span> 
  
<span data-ttu-id="90103-146">Вложенные сообщения текстизируются в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="90103-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="90103-147">Иерархия вложенных сообщений всегда плоская; то есть сообщения в вложенных сообщениях извлекаются на верхний уровень.</span><span class="sxs-lookup"><span data-stu-id="90103-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="90103-148">Внедренные объекты OLE удаляются.</span><span class="sxs-lookup"><span data-stu-id="90103-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="90103-149">Положения отрисовки вложений передаются буквально с помощью свойства **PR_ATTACH_RENDERING** ([PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)в TNEF.</span><span class="sxs-lookup"><span data-stu-id="90103-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="90103-150">Если TNEF не используется, они теряются.</span><span class="sxs-lookup"><span data-stu-id="90103-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="90103-151">Для входящих вложений без позиции отрисовки (в том числе при отсутствие TNEF) установлено положение 0xFFFFFFFF, то есть нет положения в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="90103-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90103-152">См. также</span><span class="sxs-lookup"><span data-stu-id="90103-152">See also</span></span>



[<span data-ttu-id="90103-153">Сопоставление атрибутов почты Интернета со свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="90103-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

