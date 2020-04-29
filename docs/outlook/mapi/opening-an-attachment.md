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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430625"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="a60f6-103">Открытие вложения</span><span class="sxs-lookup"><span data-stu-id="a60f6-103">Opening an attachment</span></span>

<span data-ttu-id="a60f6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a60f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a60f6-105">Открытие вложения подразумевает отображение его данных.</span><span class="sxs-lookup"><span data-stu-id="a60f6-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="a60f6-106">Например, при открытии вложения файла отображается его содержимое.</span><span class="sxs-lookup"><span data-stu-id="a60f6-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="a60f6-107">В то время как сообщения и папки открываются с помощью идентификаторов записей, вложения открываются с использованием их номеров вложений — **PR_ATTACH_NUM** свойства.</span><span class="sxs-lookup"><span data-stu-id="a60f6-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="a60f6-108">Дополнительные сведения см **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="a60f6-109">Номера вложений доступны в таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="a60f6-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="a60f6-110">Открытие всех вложений в сообщении</span><span class="sxs-lookup"><span data-stu-id="a60f6-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="a60f6-111">Вызовите метод сообщения [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) для доступа к своей таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="a60f6-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="a60f6-112">Вызовите [хркуеряллровс](hrqueryallrows.md) для получения всех строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="a60f6-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="a60f6-113">Для каждой строки:</span><span class="sxs-lookup"><span data-stu-id="a60f6-113">For each row:</span></span> 
    
    1. <span data-ttu-id="a60f6-114">Откройте вложение, передав номер вложения, представленный в столбце **PR_ATTACH_NUM** , в вызове метода **iMessage:: опенаттач** сообщения.</span><span class="sxs-lookup"><span data-stu-id="a60f6-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="a60f6-115">Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="a60f6-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="a60f6-116">**Опенаттач** возвращает указатель на реализацию **иаттач** , которая предоставляет доступ к свойствам вложений.</span><span class="sxs-lookup"><span data-stu-id="a60f6-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="a60f6-117">Вызовите метод **IMAPIProp::/PROPS** вложения для получения свойства **PR_ATTACH_METHOD** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="a60f6-118">Дополнительные сведения см. в статье [IMAPIProp::-PROPS](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="a60f6-119">Если для **PR_ATTACH_METHOD** задано значение ATTACH_BY_REF_ONLY, вызовите метод **IMAPIProp::-PROPS** для получения свойства **PR_ATTACH_PATHNAME** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="a60f6-120">Дополнительные сведения см **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="a60f6-121">Если для параметра **PR\_ATTACH_METHOD** задано\_присоединение BY_VALUE, вызовите метод **IMAPIProp:: опенпроперти** , чтобы открыть свойство **\_PR ATTACH_DATA_BIN** с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="a60f6-122">Ниже приведен пример кода, приведенного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="a60f6-122">See the sample code following this procedure.</span></span> <span data-ttu-id="a60f6-123">Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="a60f6-124">Если для параметра **PR_ATTACH_METHOD** задано значение ATTACH_OLE, а вложение является объектом OLE 2:</span><span class="sxs-lookup"><span data-stu-id="a60f6-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="a60f6-125">Call **IMAPIProp:: опенпроперти** для открытия свойства **PR\_ATTACH_DATA_OBJ** с помощью интерфейса **помощью istreamdocfile** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="a60f6-126">Попытаться использовать этот интерфейс, так как это реализация **IStream** обеспечивает работу с структурированным хранилищем с минимальным количеством издержек.</span><span class="sxs-lookup"><span data-stu-id="a60f6-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="a60f6-127">Дополнительные сведения см **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="a60f6-128">Если произошел сбой вызова **опенпроперти** , повторно вызовите его для получения свойства **PR_ATTACH_DATA_BIN** с помощью интерфейса **помощью istreamdocfile** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="a60f6-129">Если второй вызов **опенпроперти** завершается с ошибкой, попробуйте вызвать **опенпроперти** для получения **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="a60f6-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="a60f6-130">Однако вместо параметра **помощью istreamdocfile**укажите интерфейс **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="a60f6-131">Если для **PR_ATTACH_METHOD** задано значение ATTACH_EMBEDDED_MSG, нередко используется значение **PR_ATTACH_DATA_OBJ** для хранения ошибки.</span><span class="sxs-lookup"><span data-stu-id="a60f6-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="a60f6-132">Это связано с тем, что у вас и у средства реализации таблиц нет способа согласовать тип возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="a60f6-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="a60f6-133">Чтобы получить указатель на вложенное сообщение, откройте вложение с помощью **iMessage:: опенаттач**.</span><span class="sxs-lookup"><span data-stu-id="a60f6-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="a60f6-134">Затем можно получить доступ к данным вложения, вызвав метод **IMAPIProp:: опенпроперти** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="a60f6-135">Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md) and [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a60f6-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="a60f6-136">Вы можете запросить открытие вложения в режиме чтения и записи или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a60f6-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="a60f6-137">Режим "только чтение" используется по умолчанию, а многие поставщики хранилищ сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают запрос.</span><span class="sxs-lookup"><span data-stu-id="a60f6-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="a60f6-138">Передайте флаг MAPI_BEST_ACCESS, чтобы запросить предоставление поставщиком хранилища сообщений максимального уровня доступа, а затем извлеките свойство **PR_ACCESS_LEVEL** открытого вложения, чтобы определить уровень доступа, который фактически предоставлен.</span><span class="sxs-lookup"><span data-stu-id="a60f6-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="a60f6-139">Дополнительные сведения см **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a60f6-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="a60f6-140">В приведенном ниже примере показано, как открыть данные в свойстве **PR\_вложения ATTACH_DATA_BIN** .</span><span class="sxs-lookup"><span data-stu-id="a60f6-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="a60f6-141">Он выделяет указатели на два потока: один для файла и один для вложения.</span><span class="sxs-lookup"><span data-stu-id="a60f6-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="a60f6-142">Функция **опенстреамонфиле** открывает поток файлов в режиме "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="a60f6-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="a60f6-143">Вызов метода вложения **IMAPIProp:: опенпроперти** открывает поток вложений в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="a60f6-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="a60f6-144">Дополнительные сведения см **PR_ATTACH_DATA_BIN**, [опенстреамонфиле](openstreamonfile.md)и [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="a60f6-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="a60f6-145">Затем код копирует из потока файлов в поток вложений и освобождает оба потока.</span><span class="sxs-lookup"><span data-stu-id="a60f6-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
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


