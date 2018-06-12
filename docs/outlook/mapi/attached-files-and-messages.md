---
title: Вложенные файлы и сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 489930b35d24d2691c9b9fbb59b0fa95707a0618
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808052"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="3318d-103">Вложенные файлы и сообщений</span><span class="sxs-lookup"><span data-stu-id="3318d-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="3318d-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3318d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3318d-105">При использовании во время кодирования содержимого сообщения MIME с TNEF все вложения свойства и содержимое находятся в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="3318d-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="3318d-106">TNEF самого — это один двоичный вложенные файл с именем Winmail.dat в кодировке, как описано для MIME без TNEF.</span><span class="sxs-lookup"><span data-stu-id="3318d-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="3318d-107">При использовании MIME без TNEF вложенные файлы отправляются в виде содержимого части сообщений MIME.</span><span class="sxs-lookup"><span data-stu-id="3318d-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="3318d-108">Имя файла помещается в параметре *name* в заголовок *Content-type* для вложения.</span><span class="sxs-lookup"><span data-stu-id="3318d-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="3318d-109">Набор знаков для вложения переводится в параметр *charset* *типа контента* ; и content-transfer-encoding определяются сканирования содержимое всей вложения.</span><span class="sxs-lookup"><span data-stu-id="3318d-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="3318d-110">URL-адрес вложения, специально рассматриваются:</span><span class="sxs-lookup"><span data-stu-id="3318d-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="3318d-111">Если вложение — URL-адрес (вложенный файл с расширением. URL-адрес) и режим доступа, определенные в нем — анонимный FTP закодирован внешнее сообщение и содержимое файла (URL-адрес) копируется в заголовок внешних сообщений.</span><span class="sxs-lookup"><span data-stu-id="3318d-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="3318d-112">*Content-type: сообщение/external-body; тип доступа = анонимного пользователя ftp*  (Content-Transfer-Encoding: 7-разрядных предполагается.)</span><span class="sxs-lookup"><span data-stu-id="3318d-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="3318d-113">Если только 7-разрядные символы находятся и строка не превышает 140 символов в длину, вложение представляет текст в формате ASCII.</span><span class="sxs-lookup"><span data-stu-id="3318d-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="3318d-114">*Тип содержимого: text/plain; CharSet = us-ascii кодирование при передаче контента: 7-разрядных*</span><span class="sxs-lookup"><span data-stu-id="3318d-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="3318d-115">Если длинные строки или копирование 25% 8-разрядных символов обнаружены, содержимое вложения — текст и набор знаков, определяется языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="3318d-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="3318d-116">Его следует выбрать из наборов знаков, определяемыми спецификацией ISO 8859 стандартные.</span><span class="sxs-lookup"><span data-stu-id="3318d-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="3318d-117">*Content-type: text/plain; charset = ISO-8859-1*  (например)</span><span class="sxs-lookup"><span data-stu-id="3318d-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="3318d-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="3318d-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="3318d-119">Если 25% или более символов высокой бит, двоичные вложения.</span><span class="sxs-lookup"><span data-stu-id="3318d-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="3318d-120">Кодируются с помощью алгоритма Base64.</span><span class="sxs-lookup"><span data-stu-id="3318d-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="3318d-121">*Content-type: приложение/октета потока*  (по умолчанию; на основе расширения файла)</span><span class="sxs-lookup"><span data-stu-id="3318d-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="3318d-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="3318d-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="3318d-123">Для исходящих сообщений типа контента должны быть получены из трех букв расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="3318d-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="3318d-124">Это сопоставление существует в системном реестре; в этом разделе — это строковое значение с именем «Тип содержимого», задающей типу содержимого MIME, если оно было определено.</span><span class="sxs-lookup"><span data-stu-id="3318d-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="3318d-125">В этом примере — для файла изображения TIFF:</span><span class="sxs-lookup"><span data-stu-id="3318d-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="3318d-126">HKEY_LOCAL_MACHINE\\</span><span class="sxs-lookup"><span data-stu-id="3318d-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="3318d-127">Software\\</span><span class="sxs-lookup"><span data-stu-id="3318d-127">Software\\</span></span>
  
<span data-ttu-id="3318d-128">Microsoft\\</span><span class="sxs-lookup"><span data-stu-id="3318d-128">Microsoft\\</span></span>
  
<span data-ttu-id="3318d-129">Classes\\</span><span class="sxs-lookup"><span data-stu-id="3318d-129">Classes\\</span></span>
  
<span data-ttu-id="3318d-130">.tif</span><span class="sxs-lookup"><span data-stu-id="3318d-130">.tif</span></span>
  
<span data-ttu-id="3318d-131">Тип контента = «image/tiff»</span><span class="sxs-lookup"><span data-stu-id="3318d-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="3318d-132">Если отсутствует сопоставление для расширения файла, следует использовать *приложение/октета* поток по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3318d-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="3318d-133">На входящих сообщений типа контента для вложения, которое необходимо копировать всегда в свойство MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3318d-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="3318d-134">Даже в том случае, если имя файла определен для вложенного файла, расширение, сопоставленные с типом содержимого должен использоваться в свойства **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) и **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="3318d-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="3318d-135">Параметр *name* официально поддерживается, согласно документу RFC 821.</span><span class="sxs-lookup"><span data-stu-id="3318d-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="3318d-136">По мере стандартов Microsoft будут использоваться указания альтернативного сопоставления для вложенных файлов.</span><span class="sxs-lookup"><span data-stu-id="3318d-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="3318d-137">Вложенные исходящие сообщения отправляются в виде * Content-type: message/rfc822 * сообщения в рамках вложенные сообщения, закодированный рекурсивно, вместо них соответствующих прав.</span><span class="sxs-lookup"><span data-stu-id="3318d-137">Outbound attached messages are sent as * Content-type: message/rfc822 *  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="3318d-138">Входящий трафик содержимого части сообщения с *Content-Type: multipart/digest* также сопоставляются с внедренных сообщений.</span><span class="sxs-lookup"><span data-stu-id="3318d-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="3318d-139">При использовании uuencode с TNEF а кодировка содержимого сообщения все вложения свойства и содержимое находятся в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="3318d-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="3318d-140">TNEF самого — это один двоичный вложенные файл с именем Winmail.dat в кодировке, как описано для Uuencode без TNEF.</span><span class="sxs-lookup"><span data-stu-id="3318d-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="3318d-141">При использовании uuencode без TNEF все вложенные файлы обрабатывается как двоичный и формате UUENCODE, выполнив текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="3318d-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="3318d-142">Имя файла присутствует в заголовке uuencode:</span><span class="sxs-lookup"><span data-stu-id="3318d-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="3318d-143">начать 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="3318d-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="3318d-144">... данных...</span><span class="sxs-lookup"><span data-stu-id="3318d-144">... data ...</span></span> 
  
 <span data-ttu-id="3318d-145">end</span><span class="sxs-lookup"><span data-stu-id="3318d-145">end</span></span> 
  
<span data-ttu-id="3318d-146">Вложенные сообщения textized в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="3318d-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="3318d-147">Иерархия вложенные сообщения всегда сведение; то есть сообщения в рамках вложенные сообщения извлекаются на верхний уровень.</span><span class="sxs-lookup"><span data-stu-id="3318d-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="3318d-148">Внедренные объекты OLE, отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="3318d-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="3318d-149">Вложения визуализации положения передаются сам, с помощью свойства **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="3318d-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="3318d-150">Если не используется формат TNEF, они будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="3318d-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="3318d-151">Входящие вложения с не положения (в том числе при не TNEF) иметь свои положения значение 0xFFFFFFFF, то есть не позицию в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="3318d-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3318d-152">См. также</span><span class="sxs-lookup"><span data-stu-id="3318d-152">See also</span></span>



[<span data-ttu-id="3318d-153">Сопоставление атрибутов почты Интернета для свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="3318d-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

