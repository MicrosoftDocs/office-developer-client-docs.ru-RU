---
title: Присоединенные файлы и сообщения
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
# <a name="attached-files-and-messages"></a><span data-ttu-id="7642a-103">Присоединенные файлы и сообщения</span><span class="sxs-lookup"><span data-stu-id="7642a-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="7642a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7642a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7642a-105">Если MIME с TNEF используется при кодовом коде контента сообщений, все свойства и содержимое вложений находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="7642a-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="7642a-106">Сам TNEF представляет собой единый двоичный присоединенный файл winmail.dat, закодированный как описано для MIME без TNEF.</span><span class="sxs-lookup"><span data-stu-id="7642a-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="7642a-107">Если MIME используется без TNEF, присоединенные файлы отправляются в качестве частей контента сообщения MIME.</span><span class="sxs-lookup"><span data-stu-id="7642a-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="7642a-108">Имя файла помещается в  *параметре имя*  в заглавную папку  *типа Контент*  для вложения.</span><span class="sxs-lookup"><span data-stu-id="7642a-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="7642a-109">Набор символов для вложения помещается в  *параметре charset*  для  *типа Content;*  оно и кодироление переноса контента определяются путем сканирования всего содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="7642a-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="7642a-110">Вложения URL-адресов обрабатываются специально:</span><span class="sxs-lookup"><span data-stu-id="7642a-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="7642a-111">Если вложение является URL-адресом (присоединенный файл с расширением. URL-адрес), а режим доступа, определенный в нем, является анонимным FTP, кодируется как внешнее сообщение, а содержимое файла (URL-адрес) копируется в загон внешнего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7642a-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="7642a-112">*Тип контента: сообщение/внешнее тело; access-type=anon-ftp*  (предполагается контент-transfer-Encoding: 7bit).)</span><span class="sxs-lookup"><span data-stu-id="7642a-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="7642a-113">Если найдены только 7-битные символы, а длина строки не превышает 140 символов, вложение — это текст ASCII.</span><span class="sxs-lookup"><span data-stu-id="7642a-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="7642a-114">*Тип контента: текст/обычная; charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="7642a-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="7642a-115">Если найдены длинные строки или до 25% 8-битных символов, содержимое вложения является текстовым, а набор символов определяется локализом.</span><span class="sxs-lookup"><span data-stu-id="7642a-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="7642a-116">Его следует выбирать из наборов символов, определенных стандартом ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="7642a-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="7642a-117">*Тип контента: text/plain; charset=ISO-8859-1*  (например)</span><span class="sxs-lookup"><span data-stu-id="7642a-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="7642a-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="7642a-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="7642a-119">Если 25% или более символов имеют высокий бит, вложение двоично.</span><span class="sxs-lookup"><span data-stu-id="7642a-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="7642a-120">Кодируются с помощью алгоритма Base64.</span><span class="sxs-lookup"><span data-stu-id="7642a-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="7642a-121">*Тип контента: application/octet-stream*  (по умолчанию, в зависимости от расширения файла)</span><span class="sxs-lookup"><span data-stu-id="7642a-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="7642a-122">Кодинг контента-передачи: base64 \*</span><span class="sxs-lookup"><span data-stu-id="7642a-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="7642a-123">В исходящие сообщения тип контента должен быть получен из расширения файла с тремя буквами.</span><span class="sxs-lookup"><span data-stu-id="7642a-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="7642a-124">Это сопоставление существует в реестре системы; под строкой имеется значение "Тип контента", которое дает тип контента MIME, если он определен.</span><span class="sxs-lookup"><span data-stu-id="7642a-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="7642a-125">В этом примере для файла изображений TIFF:</span><span class="sxs-lookup"><span data-stu-id="7642a-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="7642a-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="7642a-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="7642a-127">Программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="7642a-127">Software</span></span>\
  
<span data-ttu-id="7642a-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="7642a-128">Microsoft</span></span>\
  
<span data-ttu-id="7642a-129">Классы</span><span class="sxs-lookup"><span data-stu-id="7642a-129">Classes</span></span>\
  
<span data-ttu-id="7642a-130">.tif</span><span class="sxs-lookup"><span data-stu-id="7642a-130">.tif</span></span>
  
<span data-ttu-id="7642a-131">Тип контента = "изображение/tiff"</span><span class="sxs-lookup"><span data-stu-id="7642a-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="7642a-132">Если нет сопоставления для расширения файла, следует использовать поток  *приложения и octet*  по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7642a-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="7642a-133">В входящие сообщения тип контента для вложения всегда должен быть **скопирован** в свойство MAPI PR_ATTACH_MIME_TAG [(PidTagAttachMimeTag).](pidtagattachmimetag-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7642a-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="7642a-134">Даже если для присоединенного файла определено имя файла, расширение, отображенное типом контента, следует использовать в свойствах **PR_ATTACH_FILENAME** [(PidTagAttachFilename)](pidtagattachfilename-canonical-property.md)и **PR_ATTACH_EXTENSION** [(PidTagAttachExtension).](pidtagattachextension-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7642a-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="7642a-135">Параметр  *имя*  официально отстает от RFC 821.</span><span class="sxs-lookup"><span data-stu-id="7642a-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="7642a-136">По мере развития стандартов Корпорация Майкрософт рассмотрит возможность указания альтернативного сопоставления для присоединенных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="7642a-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="7642a-137">Исходящие присоединенные сообщения отправляются в виде \* Типа контента: сообщения/rfc822 \* Сообщения в прикрепленных сообщениях кодируются повторно, в их надлежащем месте.</span><span class="sxs-lookup"><span data-stu-id="7642a-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="7642a-138">Входящие части контента сообщений  *с контентом типа Content-Type: multipart/digest*  также отображёны для встроенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7642a-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="7642a-139">Если uuencode с TNEF используется при кодировании контента сообщений, все свойства и содержимое вложений находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="7642a-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="7642a-140">Сам TNEF — это один двоичный присоединенный файл с именем Winmail.dat, закодированный как описано для Uuencode без TNEF.</span><span class="sxs-lookup"><span data-stu-id="7642a-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="7642a-141">Если uuencode используется без TNEF, все присоединенные файлы рассматриваются как двоичные и uuencoded, следуя тексту сообщения.</span><span class="sxs-lookup"><span data-stu-id="7642a-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="7642a-142">Имя файла присутствует в загонщике uuencode:</span><span class="sxs-lookup"><span data-stu-id="7642a-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="7642a-143">начало 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="7642a-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="7642a-144">... данные ...</span><span class="sxs-lookup"><span data-stu-id="7642a-144">... data ...</span></span> 
  
 <span data-ttu-id="7642a-145">end</span><span class="sxs-lookup"><span data-stu-id="7642a-145">end</span></span> 
  
<span data-ttu-id="7642a-146">Присоединенные сообщения текстовые в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="7642a-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="7642a-147">Иерархия присоединенных сообщений всегда выравнивается; то есть сообщения в прикрепленных сообщениях извлекаются на верхний уровень.</span><span class="sxs-lookup"><span data-stu-id="7642a-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="7642a-148">Встроенные объекты OLE удаляются.</span><span class="sxs-lookup"><span data-stu-id="7642a-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="7642a-149">Позиции отрисовки вложений передаются в буквальном смысле, **используя** свойство [PR_ATTACH_RENDERING (PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)в TNEF.</span><span class="sxs-lookup"><span data-stu-id="7642a-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="7642a-150">Если TNEF не используется, они теряются.</span><span class="sxs-lookup"><span data-stu-id="7642a-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="7642a-151">Входящие вложения без позиции отрисовки (в том числе при отсутствие TNEF) имеют свою позицию отрисовки 0xFFFFFFFF, то есть нет позиции в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="7642a-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7642a-152">См. также</span><span class="sxs-lookup"><span data-stu-id="7642a-152">See also</span></span>



[<span data-ttu-id="7642a-153">Сопоставление атрибутов интернет-почты с свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="7642a-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

