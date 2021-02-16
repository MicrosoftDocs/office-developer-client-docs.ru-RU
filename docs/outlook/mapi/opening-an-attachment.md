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
# <a name="opening-an-attachment"></a><span data-ttu-id="cd21e-103">Открытие вложения</span><span class="sxs-lookup"><span data-stu-id="cd21e-103">Opening an attachment</span></span>

<span data-ttu-id="cd21e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd21e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd21e-105">Открытие вложения включает отображение его данных.</span><span class="sxs-lookup"><span data-stu-id="cd21e-105">Opening an attachment involves displaying its data.</span></span> <span data-ttu-id="cd21e-106">Например, при открытом вложении файла отображается его содержимое.</span><span class="sxs-lookup"><span data-stu-id="cd21e-106">For example, when a file attachment is opened, the contents of the file are displayed.</span></span> <span data-ttu-id="cd21e-107">В то время как сообщения и папки открываются с использованием идентификаторов записей, вложения открываются с помощью номеров PR_ATTACH_NUM **свойств.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-107">Whereas messages and folders are opened using their entry identifiers, attachments are opened using their attachment numbers — **PR_ATTACH_NUM** properties.</span></span> <span data-ttu-id="cd21e-108">Дополнительные сведения **см. в PR_ATTACH_NUM** ([PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-108">For more information, see **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span></span> <span data-ttu-id="cd21e-109">Номера вложений доступны в таблице вложений сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-109">Attachment numbers are available through a message's attachment table.</span></span>
  
### <a name="to-open-all-attachments-in-a-message"></a><span data-ttu-id="cd21e-110">Открытие всех вложений в сообщении</span><span class="sxs-lookup"><span data-stu-id="cd21e-110">To open all attachments in a message</span></span>
  
1. <span data-ttu-id="cd21e-111">Вызовите метод [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) сообщения, чтобы получить доступ к таблице вложений.</span><span class="sxs-lookup"><span data-stu-id="cd21e-111">Call the message's [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method to access its attachment table.</span></span> 
    
2. <span data-ttu-id="cd21e-112">Вызовите [HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="cd21e-112">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all the rows in the table.</span></span> 
    
3. <span data-ttu-id="cd21e-113">Для каждой строки:</span><span class="sxs-lookup"><span data-stu-id="cd21e-113">For each row:</span></span> 
    
    1. <span data-ttu-id="cd21e-114">Откройте вложение, передав номер вложения, **представленный** в столбце PR_ATTACH_NUM в вызове метода **IMessage::OpenAttach** сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-114">Open the attachment by passing the attachment number represented in the **PR_ATTACH_NUM** column in a call to the message's **IMessage::OpenAttach** method.</span></span> <span data-ttu-id="cd21e-115">Дополнительные сведения см. в [IMessage::OpenAttach.](imessage-openattach.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-115">For more information, see [IMessage::OpenAttach](imessage-openattach.md).</span></span> <span data-ttu-id="cd21e-116">**OpenAttach** возвращает указатель на реализацию **IAttach,** которая предоставляет доступ к свойствам вложения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-116">**OpenAttach** returns a pointer to an **IAttach** implementation that provides access to attachment properties.</span></span> 
        
    2. <span data-ttu-id="cd21e-117">Вызовите метод **IMAPIProp::GetProps** вложения, чтобы получить **его PR_ATTACH_METHOD.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-117">Call the attachment's **IMAPIProp::GetProps** method to retrieve its **PR_ATTACH_METHOD** property.</span></span> <span data-ttu-id="cd21e-118">Дополнительные сведения см. в подразделе [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-118">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).</span></span>
        
    3. <span data-ttu-id="cd21e-119">Если **PR_ATTACH_METHOD** установлено ATTACH_BY_REF_ONLY, вызовите **IMAPIProp::GetProps,** чтобы **получить PR_ATTACH_PATHNAME** свойства.</span><span class="sxs-lookup"><span data-stu-id="cd21e-119">If **PR_ATTACH_METHOD** is set to ATTACH_BY_REF_ONLY, call **IMAPIProp::GetProps** to retrieve the **PR_ATTACH_PATHNAME** property.</span></span> <span data-ttu-id="cd21e-120">Дополнительные сведения **см. в PR_ATTACH_PATHNAME** ([PidTagAttachPathname).](pidtagattachpathname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-120">For more information, see **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).</span></span>
        
    4. <span data-ttu-id="cd21e-121">Если **\_ для ATTACH_METHOD** pr установлено значение ATTACH BY_VALUE, вызовите \_ **IMAPIProp::OpenProperty,** чтобы открыть свойство **PR \_** ATTACH_DATA_BIN с помощью **интерфейса IStream.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-121">If **PR\_ATTACH_METHOD** is set to ATTACH\_BY_VALUE, call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_BIN** property with the **IStream** interface.</span></span> <span data-ttu-id="cd21e-122">См. пример кода, следующего за этой процедурой.</span><span class="sxs-lookup"><span data-stu-id="cd21e-122">See the sample code following this procedure.</span></span> <span data-ttu-id="cd21e-123">Дополнительные сведения см. в подразделе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary).](pidtagattachdatabinary-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-123">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span>
        
    5. <span data-ttu-id="cd21e-124">Если **PR_ATTACH_METHOD** установлено ATTACH_OLE и вложением является объект OLE 2:</span><span class="sxs-lookup"><span data-stu-id="cd21e-124">If **PR_ATTACH_METHOD** is set to ATTACH_OLE and the attachment is an OLE 2 object:</span></span> 
        
        1. <span data-ttu-id="cd21e-125">Вызовите **IMAPIProp::OpenProperty,** чтобы открыть **ATTACH_DATA_OBJ PR \_** с помощью интерфейса **IStreamDocfile.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-125">Call **IMAPIProp::OpenProperty** to open the **PR\_ATTACH_DATA_OBJ** property with the **IStreamDocfile** interface.</span></span> <span data-ttu-id="cd21e-126">Старайтесь использовать этот интерфейс, так как это реализация **IStream,** гарантируемая для работы со структурированным хранилищем с наименьшим объемом дополнительных расходов.</span><span class="sxs-lookup"><span data-stu-id="cd21e-126">Attempt to use this interface because it is an implementation of **IStream** guaranteed to work with structured storage with the least amount of overhead.</span></span> <span data-ttu-id="cd21e-127">Дополнительные сведения **см. в PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-127">For more information, see **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).</span></span>
            
        2. <span data-ttu-id="cd21e-128">Если вызов **OpenProperty** не удается, вызовите  его еще раз, чтобы получить PR_ATTACH_DATA_BIN с интерфейсом **IStreamDocfile.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-128">If the **OpenProperty** call fails, call it again to retrieve the **PR_ATTACH_DATA_BIN** property with the **IStreamDocfile** interface.</span></span> 
            
        3. <span data-ttu-id="cd21e-129">Если второй вызов **OpenProperty** не удается, попробуйте еще раз вызвать **OpenProperty,** чтобы **PR_ATTACH_DATA_OBJ**.</span><span class="sxs-lookup"><span data-stu-id="cd21e-129">If this second **OpenProperty** call fails, try again to call **OpenProperty** to retrieve **PR_ATTACH_DATA_OBJ**.</span></span> <span data-ttu-id="cd21e-130">Однако вместо указания **IStreamDocfile** укажите **интерфейс IStorage.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-130">However, rather than specifying **IStreamDocfile**, specify the **IStorage** interface.</span></span> 
    
4. <span data-ttu-id="cd21e-131">Если **PR_ATTACH_METHOD** установлено значение ATTACH_EMBEDDED_MSG, значение PR_ATTACH_DATA_OBJ содержать ошибку. </span><span class="sxs-lookup"><span data-stu-id="cd21e-131">If **PR_ATTACH_METHOD** is set to ATTACH_EMBEDDED_MSG, it is not unusual for the value of **PR_ATTACH_DATA_OBJ** to contain an error.</span></span> <span data-ttu-id="cd21e-132">Это происходит потому, что вы и реализутель таблицы не можете согласовать тип возвращаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="cd21e-132">This is because you and the table implementer have no way to agree on the type of object to return.</span></span> <span data-ttu-id="cd21e-133">Чтобы получить указатель на вложенное сообщение, откройте вложение с помощью **IMessage::OpenAttach.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-133">To retrieve a pointer to the attached message, open the attachment using **IMessage::OpenAttach**.</span></span> <span data-ttu-id="cd21e-134">Затем для доступа к данным вложения вызывается метод **IMAPIProp::OpenProperty.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-134">Then access the attachment data by calling its **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="cd21e-135">Дополнительные сведения см. в подразделах [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-135">For more information, see [IMessage::OpenAttach](imessage-openattach.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
<span data-ttu-id="cd21e-136">Вы можете запросить открытие вложения в режиме чтения,записи или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-136">You can request that an attachment is opened in read/write or read-only mode.</span></span> <span data-ttu-id="cd21e-137">Режим "только чтение" является режимом по умолчанию, и многие поставщики хранимых сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают.</span><span class="sxs-lookup"><span data-stu-id="cd21e-137">Read-only is the default mode, and many message store providers open all attachments in this mode regardless of what clients request.</span></span> <span data-ttu-id="cd21e-138">Передай флаг MAPI_BEST_ACCESS, чтобы попросить поставщика магазина сообщений предоставить ему самый высокий уровень доступа, а затем получить свойство PR_ACCESS_LEVEL открытого вложения, чтобы определить фактически предоставленный уровень доступа. </span><span class="sxs-lookup"><span data-stu-id="cd21e-138">Pass the MAPI_BEST_ACCESS flag to request that the message store provider grant the highest level of access it can and then retrieve the open attachment's **PR_ACCESS_LEVEL** property to determine the level of access that was actually granted.</span></span> <span data-ttu-id="cd21e-139">Дополнительные сведения **см. в PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-139">For more information, see **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).</span></span>
  
<span data-ttu-id="cd21e-140">В следующем примере показано, как открыть данные в свойстве **PR \_ ATTACH_DATA_BIN вложения.**</span><span class="sxs-lookup"><span data-stu-id="cd21e-140">The following example shows how to open the data in an attachment's **PR\_ATTACH_DATA_BIN** property.</span></span> <span data-ttu-id="cd21e-141">Он выделяет указатели двум потокам: одному для файла и одному для вложения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-141">It allocates pointers to two streams: one for the file and one for the attachment.</span></span> <span data-ttu-id="cd21e-142">Функция **OpenStreamOnFile** открывает поток файлов в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cd21e-142">The **OpenStreamOnFile** function opens the file stream in read-only mode.</span></span> <span data-ttu-id="cd21e-143">Вызов метода **IMAPIProp::OpenProperty** вложения открывает поток вложений в режиме чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="cd21e-143">The call to the attachment's **IMAPIProp::OpenProperty** method opens the attachment stream in read/write mode.</span></span> <span data-ttu-id="cd21e-144">Дополнительные сведения **см. в PR_ATTACH_DATA_BIN,** [OpenStreamOnFile](openstreamonfile.md)и [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="cd21e-144">For more information, see **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md), and [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="cd21e-145">Затем код копирует из потока файлов в поток вложений и освобождает оба потока.</span><span class="sxs-lookup"><span data-stu-id="cd21e-145">The code then copies from the file stream to the attachment stream and releases both streams.</span></span>
  
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


