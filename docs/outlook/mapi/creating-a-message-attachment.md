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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332944"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="363df-103">Создание вложения к сообщению</span><span class="sxs-lookup"><span data-stu-id="363df-103">Creating a message attachment</span></span>
  
<span data-ttu-id="363df-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="363df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="363df-105">Вложение сообщения — это некоторые дополнительные данные, например файл, другое сообщение или объект OLE, которые можно отправлять и сохранять вместе с сообщением.</span><span class="sxs-lookup"><span data-stu-id="363df-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="363df-106">Каждое вложение имеет коллекцию свойств, определяющих его и описывающую его тип и способ отображения.</span><span class="sxs-lookup"><span data-stu-id="363df-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="363df-107">Как и получатели, доступ к вложениям сообщений возможен только через сообщение, к которому они относятся.</span><span class="sxs-lookup"><span data-stu-id="363df-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="363df-108">Таким образом, чтобы вложение можно было использовать, его сообщение должно быть открыто.</span><span class="sxs-lookup"><span data-stu-id="363df-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="363df-109">Создание вложения сообщения</span><span class="sxs-lookup"><span data-stu-id="363df-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="363df-110">ВыЗовите метод сообщения [iMessage:: креатеаттач](imessage-createattach.md) и передайте значение NULL в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="363df-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="363df-111">**Креатеаттач** возвращает число, которое уникально идентифицирует новое вложение в сообщении.</span><span class="sxs-lookup"><span data-stu-id="363df-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="363df-112">Номер вложения хранится в свойстве **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) и действителен только до тех пор, пока не будет открыто сообщение, содержащее вложение.</span><span class="sxs-lookup"><span data-stu-id="363df-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="363df-113">Call [IMAPIProp:: SetProps](imapiprop-setprops.md) to set **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), чтобы указать, как получить доступ к вложению.</span><span class="sxs-lookup"><span data-stu-id="363df-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="363df-114">**Пр_аттач_месод** является обязательным.</span><span class="sxs-lookup"><span data-stu-id="363df-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="363df-115">Задайте для него значение:</span><span class="sxs-lookup"><span data-stu-id="363df-115">Set it to:</span></span> 
    
   - <span data-ttu-id="363df-116">АТТАЧ_БИ_ВАЛУЕ, если вложение является двоичными данными.</span><span class="sxs-lookup"><span data-stu-id="363df-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="363df-117">АТТАЧ_БИ_РЕФЕРЕНЦЕ, АТТАЧ_БИ_РЕФ_РЕСОЛВЕ или АТТАЧ_БИ_РЕФ_ОНЛИ, если вложение является файлом.</span><span class="sxs-lookup"><span data-stu-id="363df-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="363df-118">АТТАЧ_ЕМБЕДДЕД_МСГ, если вложение является сообщением.</span><span class="sxs-lookup"><span data-stu-id="363df-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="363df-119">АТТАЧ_ОЛЕ, если вложение является объектом OLE.</span><span class="sxs-lookup"><span data-stu-id="363df-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="363df-120">Задайте соответствующее свойство данных вложения:</span><span class="sxs-lookup"><span data-stu-id="363df-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="363df-121">**Пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) для двоичных данных и объектов OLE 1.</span><span class="sxs-lookup"><span data-stu-id="363df-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="363df-122">**Пр_аттач_паснаме** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) для файлов.</span><span class="sxs-lookup"><span data-stu-id="363df-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="363df-123">**Пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) для сообщений и объектов OLE 2.</span><span class="sxs-lookup"><span data-stu-id="363df-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="363df-124">Задайте **пр_аттач_рендеринг** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)), чтобы сохранить графическое представление вложения для файла или двоичных вложений.</span><span class="sxs-lookup"><span data-stu-id="363df-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="363df-125">Не задавайте его для объектов OLE, которые хранят данные отображения для внутреннего использования или для вложенных сообщений.</span><span class="sxs-lookup"><span data-stu-id="363df-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="363df-126">Set **пр_рендеринг_поситион** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)), чтобы указать, где должно отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="363df-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="363df-127">**Пр_рендеринг_поситион** применяется только к клиентам, которые задают свойство **пр_боди** .</span><span class="sxs-lookup"><span data-stu-id="363df-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="363df-128">Если поддерживается только **пр_ртф_компрессед**, поместите в сжатый поток следующие сведения о заполнителе:</span><span class="sxs-lookup"><span data-stu-id="363df-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="363df-129">Чтобы задать **пр_рендеринг_поситион**, назначьте число, представляющее порядковое смещение в символах, с первым символом **пр_боди** 0, если вам нужно знать, где в сообщении отображается вложение, или 0xFFFFFFFF, если не Отображение вложений в **пр_боди**.</span><span class="sxs-lookup"><span data-stu-id="363df-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="363df-130">Set **пр_аттач_филенаме** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)), указывающий краткое имя файла для вложенного файла и значение **PR\_аттач_лонг_филенаме** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)), чтобы указать, что имя файла поддерживается на платформе, которая обрабатывает формат длинного имени файла.</span><span class="sxs-lookup"><span data-stu-id="363df-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="363df-131">Оба свойства являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="363df-131">Both properties are optional.</span></span> <span data-ttu-id="363df-132">Тем не менее, если вы настроили **пр_аттач_лонг_филенаме**, также задайте **пр_аттач_филенаме**.</span><span class="sxs-lookup"><span data-stu-id="363df-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="363df-133">Set **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), чтобы указать имя вложения, которое может отображаться в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="363df-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="363df-134">ПР_ДИСПЛАЙ_НАМЕ является необязательным.</span><span class="sxs-lookup"><span data-stu-id="363df-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="363df-135">Set ПР_АТТАЧ_ДАТА_БИН</span><span class="sxs-lookup"><span data-stu-id="363df-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="363df-136">Call [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="363df-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="363df-137">Если файл содержит данные, который открыт, или если требуется явный контроль над размером буфера, вызовите **IStream:: Write** в цикле, чтобы поместить данные в поток.</span><span class="sxs-lookup"><span data-stu-id="363df-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="363df-138">Кроме того, можно вызвать **опенстреамонфиле** , чтобы создать поток для доступа к файлу данных, а затем вызвать метод **IStream:: CopyTo** для копирования данных в поток, возвращенный методом **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="363df-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="363df-139">ВыЗовите метод **IStream:: Commit** нового потока.</span><span class="sxs-lookup"><span data-stu-id="363df-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="363df-140">Set ПР_АТТАЧ_ДАТА_ОБЖ</span><span class="sxs-lookup"><span data-stu-id="363df-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="363df-141">Call **IMAPIProp:: опенпроперти** , чтобы открыть свойство с помощью интерфейса **помощью istreamdocfile** , чтобы создать поток, работающий с структурированным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="363df-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="363df-142">**Помощью istreamdocfile** реализуется поставщиками хранилищ сообщений для предоставления клиентам более производительного способа хранения и извлечения структурированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="363df-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="363df-143">Интерфейс **помощью istreamdocfile** аналогичен интерфейсу **IStream**, но содержимое потока гарантированно форматируется как структурированное хранилище.</span><span class="sxs-lookup"><span data-stu-id="363df-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="363df-144">При успешном выполнении этого вызова создайте поток с теми же действиями, что и для параметра **пр_аттач_дата_бин**.</span><span class="sxs-lookup"><span data-stu-id="363df-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="363df-145">Если **опенпроперти** не удастся:</span><span class="sxs-lookup"><span data-stu-id="363df-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="363df-146">Снова выЗовите **опенпроперти** для запроса **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="363df-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="363df-147">ВыЗовите **стгопенстораже** , чтобы открыть объект OLE и возвратить объект Storage.</span><span class="sxs-lookup"><span data-stu-id="363df-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="363df-148">ВыЗовите возвращенный объект **IStorage:: CopyTo** для копирования в объект хранилища, возвращенный из **опенпроперти**.</span><span class="sxs-lookup"><span data-stu-id="363df-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="363df-149">ВыЗовите метод **IStorage: Commit нового объекта Storage:: Commit** .</span><span class="sxs-lookup"><span data-stu-id="363df-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="363df-150">Set ПР_АТТАЧ_ПАСНАМЕ</span><span class="sxs-lookup"><span data-stu-id="363df-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="363df-151">Выделите структуру [спропвалуе](spropvalue.md) , задав для члена **улпроптаг** значение **ПР_АТТАЧ_ПАСНАМЕ** и элемент **value. лпсз** , в строку символов, представляющую имя файла.</span><span class="sxs-lookup"><span data-stu-id="363df-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="363df-152">ВыЗовите метод вложения [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="363df-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="363df-153">Если ваша платформа поддерживает длинные имена файлов, задайте оба параметра: **пр_аттач_паснаме** и **пр_аттач_лонг_паснаме**.</span><span class="sxs-lookup"><span data-stu-id="363df-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="363df-154">Может потребоваться вызов операционной системы для получения короткого имени файла.</span><span class="sxs-lookup"><span data-stu-id="363df-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="363df-155">См. также</span><span class="sxs-lookup"><span data-stu-id="363df-155">See also</span></span>

- [<span data-ttu-id="363df-156">Вложения MAPI</span><span class="sxs-lookup"><span data-stu-id="363df-156">MAPI Attachments</span></span>](mapi-attachments.md)

