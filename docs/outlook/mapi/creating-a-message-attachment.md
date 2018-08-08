---
title: Создание вложения сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808243"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="12054-103">Создание вложения сообщения</span><span class="sxs-lookup"><span data-stu-id="12054-103">Creating a message attachment</span></span>
  
<span data-ttu-id="12054-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12054-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12054-105">Вложения сообщения является некоторые дополнительные данные, такие как файл, другое сообщение или OLE-объект, который вы можете отправить или сохранить, а также сообщение.</span><span class="sxs-lookup"><span data-stu-id="12054-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="12054-106">Каждый вложение содержит набор свойств, определяющий ее, а также его тип и порядок отображения.</span><span class="sxs-lookup"><span data-stu-id="12054-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="12054-107">Как получатели вложений сообщений осуществляется только по почте, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="12054-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="12054-108">Таким образом вложения для использования в его сообщение необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="12054-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="12054-109">Создание вложения сообщения</span><span class="sxs-lookup"><span data-stu-id="12054-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="12054-110">Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) сообщений и передать значение NULL в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="12054-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="12054-111">**CreateAttach** возвращает число, однозначно идентифицирующее новые вложения в сообщение.</span><span class="sxs-lookup"><span data-stu-id="12054-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="12054-112">Число вложений хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) и действителен только, пока открыта сообщение, содержащее вложение.</span><span class="sxs-lookup"><span data-stu-id="12054-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="12054-113">Вызовите [IMAPIProp::SetProps](imapiprop-setprops.md) , чтобы задать **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) для указания того, как получить доступ к вложение.</span><span class="sxs-lookup"><span data-stu-id="12054-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="12054-114">**PR_ATTACH_METHOD** является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12054-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="12054-115">Значение:</span><span class="sxs-lookup"><span data-stu-id="12054-115">Set it to:</span></span> 
    
   - <span data-ttu-id="12054-116">ATTACH_BY_VALUE, если вложение двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="12054-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="12054-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение представляет собой файл.</span><span class="sxs-lookup"><span data-stu-id="12054-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="12054-118">ATTACH_EMBEDDED_MSG, если сообщение имеет вложение.</span><span class="sxs-lookup"><span data-stu-id="12054-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="12054-119">ATTACH_OLE, если вложение является объектом OLE.</span><span class="sxs-lookup"><span data-stu-id="12054-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="12054-120">Задайте для свойства данных соответствующих вложений:</span><span class="sxs-lookup"><span data-stu-id="12054-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="12054-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) для двоичных данных и объекты OLE 1.</span><span class="sxs-lookup"><span data-stu-id="12054-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="12054-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) для файлов.</span><span class="sxs-lookup"><span data-stu-id="12054-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="12054-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) для сообщений и объекты OLE 2.</span><span class="sxs-lookup"><span data-stu-id="12054-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="12054-124">Задайте **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) для хранения графического представления вложения для файла или двоичные вложения.</span><span class="sxs-lookup"><span data-stu-id="12054-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="12054-125">Не устанавливайте его, объекты OLE, хранящих сведения о визуализации во внутренней сети, или вложенные сообщений.</span><span class="sxs-lookup"><span data-stu-id="12054-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="12054-126">Задайте **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) для указания, где должны отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="12054-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="12054-127">**PR_RENDERING_POSITION** применяется только к клиентам, которые необходимо задать свойство **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="12054-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="12054-128">Если вы поддерживаете только **PR_RTF_COMPRESSED**, поместите со следующими сведениями заполнитель в сжатый поток:</span><span class="sxs-lookup"><span data-stu-id="12054-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="12054-129">Чтобы задать **PR_RENDERING_POSITION**, назначьте либо число, представляющее порядковый номер сдвиг знака с первым символом **PR_BODY** , 0, если вам нужно знать, где в сообщение, отображаемое вложения или 0xFFFFFFFF, если он не задан Отображать вложения в **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="12054-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="12054-130">Установка **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) для указания краткое имя файла для файла вложения и **связей с Общественностью\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) для указания имени файла, как поддерживаются на платформе, обрабатывающего формат длинное имя файла.</span><span class="sxs-lookup"><span data-stu-id="12054-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="12054-131">Оба свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="12054-131">Both properties are optional.</span></span> <span data-ttu-id="12054-132">Тем не менее если значение **PR_ATTACH_LONG_FILENAME**, также необходимо задайте **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="12054-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="12054-133">Задайте **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для указания имени для вложения, которые отображаются в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="12054-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="12054-134">PR_DISPLAY_NAME не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12054-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="12054-135">Набор PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="12054-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="12054-136">Вызовите [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть свойства с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="12054-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="12054-137">Если файл содержит данные и откроется или требуется явных контролировать размер буфера, вызовите **IStream::Write** в цикле для помещения данных в поток.</span><span class="sxs-lookup"><span data-stu-id="12054-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="12054-138">Другая возможность — это вызов **OpenStreamOnFile** для создания потока для доступа к файлу данных и затем вызвать метод **IStream::CopyTo** этот поток для копирования данных в поток, возвращенный **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="12054-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="12054-139">Вызов метода **IStream::Commit** нового потока.</span><span class="sxs-lookup"><span data-stu-id="12054-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="12054-140">Набор PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="12054-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="12054-141">Вызовите **IMAPIProp::OpenProperty** , чтобы открыть свойства с помощью интерфейса **IStreamDocfile** для создания потока, который работает с структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="12054-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="12054-142">**IStreamDocfile** реализуется поставщиками хранилища сообщений для предоставления клиентам возможности более высокую производительность для хранения и извлечения структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="12054-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="12054-143">Интерфейс **IStreamDocfile** совпадает с **IStream**, но содержимое потока гарантированно быть в формате структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="12054-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="12054-144">Если этот вызов выполняется успешно, создайте потока с те же действия, описанные для настройки **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="12054-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="12054-145">В случае сбоя **OpenProperty** :</span><span class="sxs-lookup"><span data-stu-id="12054-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="12054-146">Вызов еще раз запросом для **IStorage** **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="12054-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="12054-147">Вызов **StgOpenStorage** для открытия объекта OLE и возвращает объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="12054-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="12054-148">Вызов метода **IStorage::CopyTo** объекта возвращенные хранилища для копирования объекта хранилища, возвращенные **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="12054-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="12054-149">Вызов метода **IStorage::Commit** новый объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="12054-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="12054-150">Набор PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="12054-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="12054-151">Выделить структуру [SPropValue](spropvalue.md) , установка для члена **ulPropTag** **PR_ATTACH_PATHNAME** и член **Value.LPSZ** к строке, которая представляет имя файла.</span><span class="sxs-lookup"><span data-stu-id="12054-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="12054-152">Вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) вложения.</span><span class="sxs-lookup"><span data-stu-id="12054-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="12054-153">Если система поддерживает длинные имена файлов, необходимо задайте **PR_ATTACH_PATHNAME** и **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="12054-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="12054-154">Может потребоваться внести без системы звонок, чтобы получить короткое имя файла.</span><span class="sxs-lookup"><span data-stu-id="12054-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12054-155">См. также</span><span class="sxs-lookup"><span data-stu-id="12054-155">See also</span></span>

- [<span data-ttu-id="12054-156">�������� MAPI</span><span class="sxs-lookup"><span data-stu-id="12054-156">MAPI Attachments</span></span>](mapi-attachments.md)

