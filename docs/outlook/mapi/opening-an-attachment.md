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
# <a name="opening-an-attachment"></a>Открытие вложений

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Открытие вложения включает в себя отображение его данных. Например при открытии файла вложения отображаются содержимое файла. В то время как сообщения и папки открытого с помощью их идентификаторы записей, вложения открываются с помощью своих номеров вложения — **PR_ATTACH_NUM** свойства. Для получения дополнительных сведений см **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Номера вложения доступны через таблицы вложений сообщений.
  
### <a name="to-open-all-attachments-in-a-message"></a>Чтобы открыть все вложения в сообщение
  
1. Вызов метода [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) сообщение для доступа к его вложений в таблице. 
    
2. Вызовите [HrQueryAllRows](hrqueryallrows.md) , чтобы получить все строки в таблице. 
    
3. Для каждой строки: 
    
    1. Откройте вложение, передав номер вложения, представленного в столбце **PR_ATTACH_NUM** в вызов метода **IMessage::OpenAttach** сообщение. Для получения дополнительных сведений см [IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** возвращает указатель на реализацию **IAttach** , который предоставляет доступ к свойствам вложения. 
        
    2. Вызов метода **IMAPIProp::GetProps** вложений для получения его свойство **PR_ATTACH_METHOD** . Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md) и **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Если **PR_ATTACH_METHOD** ATTACH_BY_REF_ONLY, вызовите **IMAPIProp::GetProps** для получения свойства **PR_ATTACH_PATHNAME** . Для получения дополнительных сведений см **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Если **связей с Общественностью\_ATTACH_METHOD** задано значение ПРИСОЕДИНИТЬ\_BY_VALUE, вызовите **IMAPIProp::OpenProperty** , чтобы открыть **связей с Общественностью\_ATTACH_DATA_BIN** свойства с помощью интерфейса **IStream** . Просмотрите образец кода следующую процедуру. Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Если значение **PR_ATTACH_METHOD** ATTACH_OLE и вложение является объектом OLE 2: 
        
        1. Вызовите **IMAPIProp::OpenProperty** , чтобы открыть **связей с Общественностью\_ATTACH_DATA_OBJ** свойства с помощью интерфейса **IStreamDocfile** . Попытка использовать этот интерфейс, так как они реализацию **IStream** работать с структурированного хранилища с наименьшими объем нагрузки. Для получения дополнительных сведений см **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. В случае сбоя вызова **OpenProperty** позвонить еще раз, чтобы получить свойство **PR_ATTACH_DATA_BIN** с помощью интерфейса **IStreamDocfile** . 
            
        3. В случае сбоя этой второй вызов **OpenProperty** попробуйте позвонить **OpenProperty** для извлечения **PR_ATTACH_DATA_OBJ**. Тем не менее вместо задания **IStreamDocfile**, укажите **IStorage** интерфейса. 
    
4. Если **PR_ATTACH_METHOD** ATTACH_EMBEDDED_MSG, не нестандартный для значения **PR_ATTACH_DATA_OBJ** содержит ошибку. Это так, как вы и реализации в таблице не имеют возможности согласовать тип возвращаемого объекта. Чтобы получить указатель вложенное сообщение, откройте вложение, используя **IMessage::OpenAttach**. Затем доступ к данным вложения путем вызова метода **IMAPIProp::OpenProperty** . Для получения дополнительных сведений см [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Можно запросить, что вложение открывается в режиме только для чтения или чтения и записи. Только для чтения, режим по умолчанию, а многие поставщики хранилища сообщений откройте все вложения в этом режиме независимо от того, клиенты запрашивают. Передайте флаг MAPI_BEST_ACCESS для запроса, что поставщик хранения сообщений предоставить высший уровень доступа, его можно, а затем извлекать свойство **PR_ACCESS_LEVEL** открыть вложение для определения уровня доступа, которые фактически были предоставлены. Для получения дополнительных сведений см **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Следующем примере показано, как открыть данные во вложении электронной **связей с Общественностью\_ATTACH_DATA_BIN** свойство. Выделяет указатели на два потока: один для файла, а другая — для вложения. Функция **OpenStreamOnFile** открывает поток файла в режиме только для чтения. Вызов метода **IMAPIProp::OpenProperty** вложения открывает поток вложения в режиме чтения и записи. Для получения дополнительных сведений см **PR_ATTACH_DATA_BIN**, [OpenStreamOnFile](openstreamonfile.md)и [IMAPIProp::OpenProperty](imapiprop-openproperty.md). В коде копирует в потоке файла вложения и освобождает обоих потоков.
  
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


