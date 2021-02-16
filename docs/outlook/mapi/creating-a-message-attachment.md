---
title: Создание вложения к сообщению
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405998"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="6ceb0-103">Создание вложения к сообщению</span><span class="sxs-lookup"><span data-stu-id="6ceb0-103">Creating a message attachment</span></span>
  
<span data-ttu-id="6ceb0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ceb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ceb0-105">Вложение сообщения — это некоторые дополнительные данные, такие как файл, другое сообщение или объект OLE, которые можно отправить или сохранить вместе с сообщением.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="6ceb0-106">Каждое вложение имеет коллекцию свойств, идентифицирует его и описывает его тип и его отрисовку.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="6ceb0-107">Как и для получателей, доступ к вложениям сообщений можно получить только через сообщение, к которому они принадлежат.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="6ceb0-108">Следовательно, чтобы вложение можно было использовать, его сообщение должно быть открыто.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="6ceb0-109">Создание вложения сообщения</span><span class="sxs-lookup"><span data-stu-id="6ceb0-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="6ceb0-110">Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) сообщения и передайте NULL в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="6ceb0-111">**CreateAttach** возвращает номер, однозначно определяя новое вложение в сообщении.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="6ceb0-112">Номер вложения хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)и действителен, только если открыто сообщение с вложением.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="6ceb0-113">Вызовите [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы PR_ATTACH_METHOD ([PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)чтобы указать, как получить доступ к вложение. </span><span class="sxs-lookup"><span data-stu-id="6ceb0-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="6ceb0-114">**PR_ATTACH_METHOD** требуется.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="6ceb0-115">Установите для него 24-е.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-115">Set it to:</span></span> 
    
   - <span data-ttu-id="6ceb0-116">ATTACH_BY_VALUE, является ли вложение двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="6ceb0-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение является файлом.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="6ceb0-118">ATTACH_EMBEDDED_MSG, является ли вложение сообщением.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="6ceb0-119">ATTACH_OLE, если вложение является объектом OLE.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="6ceb0-120">Установите соответствующее свойство данных вложения:</span><span class="sxs-lookup"><span data-stu-id="6ceb0-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="6ceb0-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)для двоичных данных и объектов OLE 1.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="6ceb0-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)для файлов.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="6ceb0-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)для сообщений и объектов OLE 2.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="6ceb0-124">**Задайте PR_ATTACH_RENDERING** ([PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)для удержания графического представления вложения для файлов или двоичных вложений.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="6ceb0-125">Не устанавливать его для объектов OLE, в которых хранятся сведения об отрисовке внутри организации или для вложенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="6ceb0-126">Зада **PR_RENDERING_POSITION** ([PidTagRenderingPosition),](pidtagrenderingposition-canonical-property.md)чтобы указать, где должно отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="6ceb0-127">**PR_RENDERING_POSITION** применяется только к клиентам, которые PR_BODY **свойства.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="6ceb0-128">Если вы поддерживаете только **PR_RTF_COMPRESSED,** поместите в сжатый поток следующие данные-замессыщики:</span><span class="sxs-lookup"><span data-stu-id="6ceb0-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="6ceb0-129">Чтобы задать **PR_RENDERING_POSITION,** назначьте либо число, которое представляет порядковую смещение символов, с первым символом **PR_BODY** 0, если вам нужно знать, где в сообщении отрисовка вложения, или 0xFFFFFFFF, если не отрисовка вложений в PR_BODY **.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="6ceb0-130">Установите **PR_ATTACH_FILENAME** ([PidTagAttachFilename),](pidtagattachfilename-canonical-property.md)чтобы указать короткое имя файла для вложенного файла и **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename),](pidtagattachlongfilename-canonical-property.md)чтобы указать имя файла, поддерживаемого на платформе, которая обрабатывает длинный формат имени файла.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="6ceb0-131">Оба свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-131">Both properties are optional.</span></span> <span data-ttu-id="6ceb0-132">Однако, если вы **PR_ATTACH_LONG_FILENAME,** также **установите** PR_ATTACH_FILENAME .</span><span class="sxs-lookup"><span data-stu-id="6ceb0-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="6ceb0-133">**Задайте PR_DISPLAY_NAME** ([PidTagDisplayName),](pidtagdisplayname-canonical-property.md)чтобы указать имя вложения, которое может отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="6ceb0-134">PR_DISPLAY_NAME необязательный.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-pr_attach_data_bin"></a><span data-ttu-id="6ceb0-135">Настройка PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="6ceb0-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="6ceb0-136">Вызовите [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство с помощью **интерфейса IStream.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="6ceb0-137">Если файл содержит данные и он открыт или требуется явный контроль над размером буфера, вызовите **IStream::Write** в цикле, чтобы разместить данные в потоке.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="6ceb0-138">Другой вариант — вызвать **OpenStreamOnFile,** чтобы создать поток для доступа к файлу данных, а затем вызвать метод **IStream::CopyTo** этого потока, чтобы скопировать данные в поток, возвращенный **OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="6ceb0-139">Вызовите метод **IStream::Commit** нового потока.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-pr_attach_data_obj"></a><span data-ttu-id="6ceb0-140">Настройка PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="6ceb0-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="6ceb0-141">Вызовите **IMAPIProp::OpenProperty,** чтобы открыть свойство с помощью интерфейса **IStreamDocfile,** чтобы создать поток, который работает со структурированным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="6ceb0-142">**IStreamDocfile** реализуется поставщиками хранилища сообщений, чтобы предоставить клиентам более высокий способ хранения и извлечения структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="6ceb0-143">Интерфейс **IStreamDocfile** такой же, как **IStream,** но содержимое потока гарантированно будет отформатировано как структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="6ceb0-144">Если этот вызов будет успешным, создайте поток, выполив те же действия, что и **PR_ATTACH_DATA_BIN.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="6ceb0-145">Если **сбой OpenProperty:**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="6ceb0-146">Снова **вызовите OpenProperty** с запросом **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="6ceb0-147">Вызовите **StgOpenStorage,** чтобы открыть объект OLE и вернуть объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="6ceb0-148">Вызовите метод **IStorage::CopyTo** возвращенного объекта хранилища, чтобы скопировать его в объект хранилища, возвращенный **из OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="6ceb0-149">Вызовите метод **IStorage::Commit** нового объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-pr_attach_pathname"></a><span data-ttu-id="6ceb0-150">Настройка PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="6ceb0-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="6ceb0-151">Выделите структуру [SPropValue,](spropvalue.md) установив для члена **ulPropTag** значение **PR_ATTACH_PATHNAME,** а для параметра **Value.LPSZ** строку символов, которая представляет имя файла.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="6ceb0-152">Вызовите метод [IMAPIProp::SetProps вложения.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="6ceb0-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6ceb0-153">Если платформа поддерживает длинные имена файлов, установите и **PR_ATTACH_PATHNAME,** и **PR_ATTACH_LONG_PATHNAME.**</span><span class="sxs-lookup"><span data-stu-id="6ceb0-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="6ceb0-154">Для получения короткого имени файла может потребоваться вызов операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6ceb0-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ceb0-155">См. также</span><span class="sxs-lookup"><span data-stu-id="6ceb0-155">See also</span></span>

- [<span data-ttu-id="6ceb0-156">MAPI Attachments</span><span class="sxs-lookup"><span data-stu-id="6ceb0-156">MAPI Attachments</span></span>](mapi-attachments.md)

