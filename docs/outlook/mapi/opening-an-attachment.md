---
title: Открытие вложения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326175"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="0fa1d-103">Открытие вложения</span><span class="sxs-lookup"><span data-stu-id="0fa1d-103">Opening an attachment</span></span>

<span data-ttu-id="0fa1d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0fa1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0fa1d-105">Открытие вложения подразумевает отображение его данных.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="0fa1d-106">Например, при открытии вложения файла отображается его содержимое.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="0fa1d-107">В то время как сообщения и папки открываются с помощью идентификаторов записей, вложения открываются с использованием их номеров вложений — свойств **пр_аттач_нум** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="0fa1d-108">Дополнительные сведения см. в статье **пр_аттач_нум** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="0fa1d-109">Номера вложений доступны в таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="0fa1d-110">Открытие всех вложений в сообщении</span><span class="sxs-lookup"><span data-stu-id="0fa1d-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="0fa1d-111">ВыЗовите метод сообщения [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) для доступа к своей таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="0fa1d-112">ВыЗовите [хркуеряллровс](hrqueryallrows.md) для получения всех строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="0fa1d-113">Для каждой строки:</span><span class="sxs-lookup"><span data-stu-id="0fa1d-113">For each row:</span></span> 
    
    1. <span data-ttu-id="0fa1d-114">Откройте вложение, передав номер вложения, представленный в столбце **пр_аттач_нум** , в вызове метода **iMessage:: опенаттач** сообщения.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="0fa1d-115">Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="0fa1d-116">**Опенаттач** возвращает указатель на реализацию **иаттач** , которая предоставляет доступ к свойствам вложений.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="0fa1d-117">ВыЗовите метод **IMAPIProp::** /PROPS вложения, чтобы получить свойство **пр_аттач_месод** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="0fa1d-118">Дополнительные сведения см. в статье [IMAPIProp::](imapiprop-getprops.md) -PROPS and **пр_аттач_месод** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="0fa1d-119">Если для **пр_аттач_месод** задано значение аттач_би_реф_онли, вызовите метод **IMAPIProp::** -Props, чтобы получить свойство \*\*пр_аттач_паснаме\*\* .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="0fa1d-120">Дополнительные сведения см. в статье **пр_аттач_паснаме** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="0fa1d-121">Если для параметра **PR\_аттач_месод** задано\_присоединение би_валуе, вызовите **IMAPIProp:: опенпроперти** , чтобы открыть свойство \*\*\_PR аттач_дата_бин\*\* с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="0fa1d-122">Ниже приведен пример кода, приведенного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-122">See the sample code following this procedure.</span></span> <span data-ttu-id="0fa1d-123">Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="0fa1d-124">Если для **пр_аттач_месод** задано значение аттач_оле, а вложение является объектом OLE 2:</span><span class="sxs-lookup"><span data-stu-id="0fa1d-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="0fa1d-125">Call **IMAPIProp:: опенпроперти** , чтобы открыть **свойство\_PR аттач_дата_обж** с интерфейсом **помощью istreamdocfile** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="0fa1d-126">ПоПытаться использовать этот интерфейс, так как это реализация **IStream** обеспечивает работу с структурированным хранилищем с минимальным количеством издержек.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="0fa1d-127">Дополнительные сведения см. в статье **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="0fa1d-128">Если произошел сбой вызова **опенпроперти** , повторно вызовите его, чтобы получить свойство **пр_аттач_дата_бин** с помощью интерфейса **помощью istreamdocfile** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="0fa1d-129">Если второй вызов **опенпроперти** завершается с ошибкой, попробуйте вызвать **Опенпроперти** для получения **пр_аттач_дата_обж**.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="0fa1d-130">Однако вместо параметра **помощью istreamdocfile**укажите интерфейс **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="0fa1d-131">Если для **пр_аттач_месод** задано значение аттач_ембеддед_мсг, нередко используется значение **пр_аттач_дата_обж** для хранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="0fa1d-132">Это связано с тем, что у вас и у средства реализации таблиц нет способа согласовать тип возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="0fa1d-133">Чтобы получить указатель на вложенное сообщение, откройте вложение с помощью **iMessage:: опенаттач**.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="0fa1d-134">Затем можно получить доступ к данным вложения, вызвав метод **IMAPIProp:: опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="0fa1d-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="0fa1d-135">Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md) and [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="0fa1d-136">Вы можете запросить открытие вложения в режиме чтения и записи или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="0fa1d-137">Режим "только чтение" используется по умолчанию, а многие поставщики хранилищ сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают запрос.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="0fa1d-138">Передайте флаг МАПИ_БЕСТ_АКЦЕСС, чтобы запросить предоставление поставщиком хранилища сообщений максимального уровня доступа, а затем извлеките свойство **пр_акцесс_левел** открытого вложения, чтобы определить уровень доступа, который фактически предоставлен.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="0fa1d-139">Дополнительные сведения см. в статье **пр_акцесс_левел** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="0fa1d-140">В приведенном ниже примере показано, как открыть данные в свойстве **\_аттач_дата_бин** для вложения.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="0fa1d-141">Он выделяет указатели на два потока: один для файла и один для вложения.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="0fa1d-142">Функция **опенстреамонфиле** открывает поток файлов в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="0fa1d-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="0fa1d-143">Вызов метода вложения **IMAPIProp:: опенпроперти** открывает поток вложений в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="0fa1d-144">Дополнительные сведения см. в статье **пр_аттач_дата_бин**, [опенстреамонфиле](openstreamonfile.md)и [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0fa1d-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="0fa1d-145">Затем код копирует из потока файлов в поток вложений и освобождает оба потока.</span><span class="sxs-lookup"><span data-stu-id="0fa1d-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


