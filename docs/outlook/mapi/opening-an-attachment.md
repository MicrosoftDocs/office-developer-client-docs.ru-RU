---
title: Открытие вложений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 768528c59d7aa5888c0d0427f86b8be8e1d33669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579979"
---
# <a name="opening-an-attachment"></a><span data-ttu-id="0f536-103">Открытие вложений</span><span class="sxs-lookup"><span data-stu-id="0f536-103">Opening an attachment</span></span>

<span data-ttu-id="0f536-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f536-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f536-105">Открытие вложения включает в себя отображение его данных.</span><span class="sxs-lookup"><span data-stu-id="0f536-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="0f536-106">Например при открытии файла вложения отображаются содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="0f536-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="0f536-107">В то время как сообщения и папки открытого с помощью их идентификаторы записей, вложения открываются с помощью своих номеров вложения — **PR_ATTACH_NUM** свойства.</span><span class="sxs-lookup"><span data-stu-id="0f536-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="0f536-108">Для получения дополнительных сведений см **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="0f536-109">Номера вложения доступны через таблицы вложений сообщений.</span><span class="sxs-lookup"><span data-stu-id="0f536-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="0f536-110">Чтобы открыть все вложения в сообщение</span><span class="sxs-lookup"><span data-stu-id="0f536-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="0f536-111">Вызов метода [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) сообщение для доступа к его вложений в таблице.</span><span class="sxs-lookup"><span data-stu-id="0f536-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="0f536-112">Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="0f536-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="0f536-113">Для каждой строки:</span><span class="sxs-lookup"><span data-stu-id="0f536-113">For each row:</span></span> 
    
    1. <span data-ttu-id="0f536-114">Откройте вложение, передав номер вложения, представленного в столбце **PR_ATTACH_NUM** в вызов метода **IMessage::OpenAttach** сообщение.</span><span class="sxs-lookup"><span data-stu-id="0f536-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="0f536-115">Для получения дополнительных сведений см [IMessage::OpenAttach](imessage-openattach.md).</span><span class="sxs-lookup"><span data-stu-id="0f536-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="0f536-116">**OpenAttach** возвращает указатель на реализацию **IAttach** , который предоставляет доступ к свойствам вложения.</span><span class="sxs-lookup"><span data-stu-id="0f536-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="0f536-117">Вызов метода **IMAPIProp::GetProps** вложений для получения его свойство **PR_ATTACH_METHOD** .</span><span class="sxs-lookup"><span data-stu-id="0f536-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="0f536-118">Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md) и **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="0f536-119">Если **PR_ATTACH_METHOD** ATTACH_BY_REF_ONLY, вызовите **IMAPIProp::GetProps** для получения свойства **PR_ATTACH_PATHNAME** .</span><span class="sxs-lookup"><span data-stu-id="0f536-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="0f536-120">Для получения дополнительных сведений см **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="0f536-121">Если **связей с Общественностью\_ATTACH_METHOD** задано значение ПРИСОЕДИНИТЬ\_BY_VALUE, вызовите **IMAPIProp::OpenProperty** , чтобы открыть **связей с Общественностью\_ATTACH_DATA_BIN** свойства с помощью интерфейса **IStream** .</span><span class="sxs-lookup"><span data-stu-id="0f536-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="0f536-122">Просмотрите образец кода следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="0f536-122">See the sample code following this procedure.</span></span> <span data-ttu-id="0f536-123">Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="0f536-124">Если значение **PR_ATTACH_METHOD** ATTACH_OLE и вложение является объектом OLE 2:</span><span class="sxs-lookup"><span data-stu-id="0f536-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="0f536-125">Вызовите **IMAPIProp::OpenProperty** , чтобы открыть **связей с Общественностью\_ATTACH_DATA_OBJ** свойства с помощью интерфейса **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="0f536-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="0f536-126">Попытка использовать этот интерфейс, так как они реализацию **IStream** работать с структурированного хранилища с наименьшими объем нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0f536-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="0f536-127">Для получения дополнительных сведений см **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="0f536-128">В случае сбоя вызова **OpenProperty** позвонить еще раз, чтобы получить свойство **PR_ATTACH_DATA_BIN** с помощью интерфейса **IStreamDocfile** .</span><span class="sxs-lookup"><span data-stu-id="0f536-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="0f536-129">В случае сбоя этой второй вызов **OpenProperty** попробуйте позвонить **OpenProperty** для извлечения **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="0f536-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="0f536-130">Тем не менее вместо задания **IStreamDocfile**, укажите **IStorage** интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0f536-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="0f536-131">Если **PR_ATTACH_METHOD** ATTACH_EMBEDDED_MSG, не нестандартный для значения **PR_ATTACH_DATA_OBJ** содержит ошибку.</span><span class="sxs-lookup"><span data-stu-id="0f536-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="0f536-132">Это так, как вы и реализации в таблице не имеют возможности согласовать тип возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0f536-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="0f536-133">Чтобы получить указатель вложенное сообщение, откройте вложение, используя **IMessage::OpenAttach**.</span><span class="sxs-lookup"><span data-stu-id="0f536-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="0f536-134">Затем доступ к данным вложения путем вызова метода **IMAPIProp::OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="0f536-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="0f536-135">Для получения дополнительных сведений см [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0f536-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="0f536-136">Можно запросить, что вложение открывается в режиме только для чтения или чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0f536-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="0f536-137">Только для чтения, режим по умолчанию, а многие поставщики хранилища сообщений откройте все вложения в этом режиме независимо от того, клиенты запрашивают.</span><span class="sxs-lookup"><span data-stu-id="0f536-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="0f536-138">Передайте флаг MAPI_BEST_ACCESS для запроса, что поставщик хранения сообщений предоставить высший уровень доступа, его можно, а затем извлекать свойство **PR_ACCESS_LEVEL** открыть вложение для определения уровня доступа, которые фактически были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="0f536-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="0f536-139">Для получения дополнительных сведений см **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f536-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="0f536-140">Следующем примере показано, как открыть данные во вложении электронной **связей с Общественностью\_ATTACH_DATA_BIN** свойство.</span><span class="sxs-lookup"><span data-stu-id="0f536-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="0f536-141">Выделяет указатели на два потока: один для файла, а другая — для вложения.</span><span class="sxs-lookup"><span data-stu-id="0f536-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="0f536-142">Функция **OpenStreamOnFile** открывает поток файла в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f536-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="0f536-143">Вызов метода **IMAPIProp::OpenProperty** вложения открывает поток вложения в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0f536-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="0f536-144">Для получения дополнительных сведений см **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)и [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0f536-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="0f536-145">В коде копирует в потоке файла вложения и освобождает обоих потоков.</span><span class="sxs-lookup"><span data-stu-id="0f536-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
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


