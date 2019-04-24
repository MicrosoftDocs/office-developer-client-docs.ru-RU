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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318132"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="75954-103">Вложенные файлы и сообщения</span><span class="sxs-lookup"><span data-stu-id="75954-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="75954-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75954-105">Если при кодировании содержимого сообщения используется MIME с ФОРМАТом TNEF, все свойства и содержимое вложений находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="75954-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="75954-106">ФОРМАТ TNEF сам по себе представляет собой отдельный двоичный файл Winmail. dat, закодированный как описанный для MIME без формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="75954-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="75954-107">Если MIME используется без формата TNEF, вложенные файлы отправляются как части MIME-содержимого сообщений.</span><span class="sxs-lookup"><span data-stu-id="75954-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="75954-108">Имя файла помещается в параметр *Name* в заголовок *Content-Type* для вложения.</span><span class="sxs-lookup"><span data-stu-id="75954-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="75954-109">Набор знаков для вложения размещается в параметре *CharSet* для *Content-Type* ; Он и кодирование контента зависят от сканирования всего содержимого вложения.</span><span class="sxs-lookup"><span data-stu-id="75954-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="75954-110">Вложения URL-адресов имеют особую отсебе:</span><span class="sxs-lookup"><span data-stu-id="75954-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="75954-111">Если вложение является URL-АДРЕСом (вложенный файл с расширением. URL-адрес), а режим доступа, определенный в нем анонимный FTP, он кодируется как внешнее сообщение, а содержимое файла (URL-адрес) копируется в заголовок внешнего сообщения.</span><span class="sxs-lookup"><span data-stu-id="75954-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="75954-112">*Content-Type: Message/External-Body; Access-Type = Анон-FTP*  (Content-Transfer-Encoding: 7bit предполагается.)</span><span class="sxs-lookup"><span data-stu-id="75954-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="75954-113">Если найдены только 7-разрядные символы, и длина строки не превышает 140 символов, то вложение будет ASCII-текст.</span><span class="sxs-lookup"><span data-stu-id="75954-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="75954-114">*Content-Type: text/plain; charset = US – ASCII Content — Transfer – Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="75954-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="75954-115">Если найдены длинные строки или до 25% 8-разрядных символов, содержимое вложения будет текстовым, а набор знаков будет определяться языковым стандартом.</span><span class="sxs-lookup"><span data-stu-id="75954-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="75954-116">Он должен быть выбран из наборов символов, определенных стандартом ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="75954-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="75954-117">*Content-Type: text/plain; charset = ISO-8859-1*  (например,)</span><span class="sxs-lookup"><span data-stu-id="75954-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="75954-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="75954-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="75954-119">Если для 25% или более символов задана Высокая скорость, вложение будет двоичным.</span><span class="sxs-lookup"><span data-stu-id="75954-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="75954-120">Он кодируется с помощью алгоритма Base64.</span><span class="sxs-lookup"><span data-stu-id="75954-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="75954-121">*Content-Type: Application/октет-Stream*  (по умолчанию; в зависимости от расширения файла)</span><span class="sxs-lookup"><span data-stu-id="75954-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="75954-122">Content — Transfer — Encoding: Base64 \*</span><span class="sxs-lookup"><span data-stu-id="75954-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="75954-123">В исходящих сообщениях тип контента должен быть производным от третьего расширения имени файла.</span><span class="sxs-lookup"><span data-stu-id="75954-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="75954-124">Это сопоставление существует в системном реестре; в разделе существует строковое значение с именем "тип контента", которое предоставляет тип контента MIME, если он определен.</span><span class="sxs-lookup"><span data-stu-id="75954-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="75954-125">Этот пример предназначен для файла изображения TIFF:</span><span class="sxs-lookup"><span data-stu-id="75954-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="75954-126">Раздел</span><span class="sxs-lookup"><span data-stu-id="75954-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="75954-127">По</span><span class="sxs-lookup"><span data-stu-id="75954-127">Software\\</span></span>
  
<span data-ttu-id="75954-128">Корпораци</span><span class="sxs-lookup"><span data-stu-id="75954-128">Microsoft\\</span></span>
  
<span data-ttu-id="75954-129">Классы</span><span class="sxs-lookup"><span data-stu-id="75954-129">Classes\\</span></span>
  
<span data-ttu-id="75954-130">TIF</span><span class="sxs-lookup"><span data-stu-id="75954-130">.tif</span></span>
  
<span data-ttu-id="75954-131">Тип контента = "Image/TIFF"</span><span class="sxs-lookup"><span data-stu-id="75954-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="75954-132">Если сопоставление для расширения файла отсутствует, следует использовать поток *приложения и октета* по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="75954-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="75954-133">Во входящих сообщениях тип контента для вложения всегда должен копироваться в свойство MAPI **пр_аттач_миме_таг** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="75954-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="75954-134">Даже если для вложенного файла определено имя файла, в свойствах **пр_аттач_филенаме** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) и **пр_аттач_екстенсион** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) необходимо использовать расширение, сопоставленное с типом контента. .</span><span class="sxs-lookup"><span data-stu-id="75954-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="75954-135">Параметр *Name* официально устарел в соответствии со спецификацией RFC 821.</span><span class="sxs-lookup"><span data-stu-id="75954-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="75954-136">По мере развития стандартов Корпорация Майкрософт рассматривает указание альтернативного сопоставления для присоединенных имен файлов.</span><span class="sxs-lookup"><span data-stu-id="75954-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="75954-137">ИсХодящие вложенные сообщения отправляются в виде \* Content-Type: сообщения/RFC822 \* сообщения в вложенных сообщениях кодируются рекурсивно в надлежащем месте.</span><span class="sxs-lookup"><span data-stu-id="75954-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="75954-138">Части контента входящих сообщений с *Content-Type: multipart/Digest* также сопоставляются с внедренными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="75954-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="75954-139">Если при кодировании содержимого сообщения используется uuencode с ФОРМАТом TNEF, все свойства и содержимое вложений находятся в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="75954-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="75954-140">ФОРМАТ TNEF сам по себе является отдельным двоичным файлом Winmail. dat, который кодируется в соответствии с описанием для uuencode без формата TNEF.</span><span class="sxs-lookup"><span data-stu-id="75954-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="75954-141">Если кодировка UUEncode используется без формата TNEF, все вложенные файлы обрабатываются как двоичные и ууенкодед, после текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="75954-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="75954-142">Имя файла присутствует в заголовке uuencode:</span><span class="sxs-lookup"><span data-stu-id="75954-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="75954-143">Начало 0755 Winmail. dat</span><span class="sxs-lookup"><span data-stu-id="75954-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="75954-144">... данные...</span><span class="sxs-lookup"><span data-stu-id="75954-144">... data ...</span></span> 
  
 <span data-ttu-id="75954-145">end</span><span class="sxs-lookup"><span data-stu-id="75954-145">end</span></span> 
  
<span data-ttu-id="75954-146">Вложенные сообщения выводятся в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="75954-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="75954-147">Иерархия вложенных сообщений всегда сведена; то есть сообщения в прикрепленных сообщениях отправляются на верхний уровень.</span><span class="sxs-lookup"><span data-stu-id="75954-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="75954-148">Внедренные объекты OLE отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="75954-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="75954-149">Позиции отображения вложений передаются буквально, используя свойство **пр_аттач_рендеринг** ([PIDTAGATTACHRENDERING](pidtagattachrendering-canonical-property.md)) в формате TNEF.</span><span class="sxs-lookup"><span data-stu-id="75954-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="75954-150">Если формат TNEF не используется, они теряются.</span><span class="sxs-lookup"><span data-stu-id="75954-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="75954-151">Для входящих вложений без позиции отрисовки (в том случае, когда отсутствует формат TNEF) позиция отображения в тексте сообщения не задана.</span><span class="sxs-lookup"><span data-stu-id="75954-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75954-152">См. также</span><span class="sxs-lookup"><span data-stu-id="75954-152">See also</span></span>



[<span data-ttu-id="75954-153">Сопоставление атрибутов почты Интернета со свойствами MAPI</span><span class="sxs-lookup"><span data-stu-id="75954-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

