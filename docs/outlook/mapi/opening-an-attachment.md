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
# <a name="opening-an-attachment"></a>Открытие вложения

**Область применения**: Outlook 2013 | Outlook 2016 
  
Открытие вложения включает отображение данных. Например, при вложении файла отображается содержимое файла. Если сообщения и папки открываются с помощью идентификаторов записей, то вложения открываются с помощью номеров **вложений** — PR_ATTACH_NUM свойств. Дополнительные сведения см. **в PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) Номера вложений доступны в таблице вложений сообщения.
  
### <a name="to-open-all-attachments-in-a-message"></a>Открытие всех вложений в сообщении
  
1. Чтобы получить доступ к таблице вложений, позвоните в [метод IMessage::GetAttachmentTable.](imessage-getattachmenttable.md) 
    
2. Позвоните [в HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице. 
    
3. Для каждой строки: 
    
    1. Откройте вложение, передав номер **вложения, представленный** в столбце PR_ATTACH_NUM в вызове к методу **IMessage::OpenAttach** сообщения. Дополнительные сведения см. [в странице IMessage::OpenAttach](imessage-openattach.md). **OpenAttach** возвращает указатель для реализации **IAttach,** которая предоставляет доступ к свойствам вложения. 
        
    2. Чтобы получить свойство **IMAPIProp::GetProps,** позвоните **по вызову PR_ATTACH_METHOD вложения.** Дополнительные сведения см. в [странице IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** [(PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)
        
    3. Если **PR_ATTACH_METHOD** установлено ATTACH_BY_REF_ONLY, позвоните **в IMAPIProp::GetProps** для получения **PR_ATTACH_PATHNAME** свойства. Дополнительные сведения см. **в PR_ATTACH_PATHNAME** [(PidTagAttachPathname).](pidtagattachpathname-canonical-property.md)
        
    4. Если **\_ ATTACH_METHOD** pr установлено значение ATTACH BY_VALUE, позвоните \_ в **IMAPIProp::OpenProperty,** чтобы открыть свойство PR ATTACH_DATA_BIN с интерфейсом **IStream.** **\_** См. пример кода, следующего за этой процедурой. Дополнительные сведения см. [в странице IMAPIProp::OpenProperty](imapiprop-openproperty.md) **и PR_ATTACH_DATA_BIN** [(PidTagAttachDataBinary).](pidtagattachdatabinary-canonical-property.md)
        
    5. Если **PR_ATTACH_METHOD** установлено ATTACH_OLE и вложение является объектом OLE 2: 
        
        1. Вызов **IMAPIProp::OpenProperty,** **чтобы \_** открыть ATTACH_DATA_OBJ pr с интерфейсом **IStreamDocfile.** Попытка использовать этот интерфейс, так как это реализация **IStream,** гарантированно работа с структурированным хранилищем с наименьшим количеством накладных расходов. Дополнительные сведения см. **в PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)
            
        2. Если вызов **OpenProperty** сбой, вызов его снова, **чтобы** получить PR_ATTACH_DATA_BIN с **интерфейсом IStreamDocfile.** 
            
        3. Если второй вызов **OpenProperty** сбой, попробуйте еще раз вызвать **OpenProperty,** чтобы **PR_ATTACH_DATA_OBJ**. Однако вместо указания **IStreamDocfile** укажите **интерфейс IStorage.** 
    
4. Если **PR_ATTACH_METHOD** установлено значение ATTACH_EMBEDDED_MSG, значение PR_ATTACH_DATA_OBJ содержит ошибку.  Это происходит из-за того, что у вас и у реализации таблицы нет способа договориться о типе возвращаемого объекта. Чтобы получить указатель на прикрепленное сообщение, откройте вложение с **помощью IMessage::OpenAttach**. Затем получить доступ к данным вложения, позвонив по **методу IMAPIProp::OpenProperty.** Дополнительные сведения см. [в странице IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
Вы можете запросить открытие вложения в режиме чтения или записи или только для чтения. Только для чтения — это режим по умолчанию, и многие поставщики магазинов сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают. Передай флаг MAPI_BEST_ACCESS, чтобы предоставить поставщику магазина сообщений наивысший уровень доступа, который он может получить, а затем получить свойство PR_ACCESS_LEVEL открытого **вложения,** чтобы определить уровень доступа, который был фактически предоставлен. Дополнительные сведения см. **в PR_ACCESS_LEVEL** [(PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
  
В следующем примере показано, как открыть данные в свойстве **\_ PR ATTACH_DATA_BIN приложения.** Он выделяет указатели на два потока: один для файла и один для вложения. Функция **OpenStreamOnFile** открывает поток файлов в режиме только для чтения. Вызов метода **IMAPIProp::OpenProperty** открывает поток вложений в режиме чтения и записи. Дополнительные сведения см. **в PR_ATTACH_DATA_BIN,** [OpenStreamOnFile](openstreamonfile.md)и [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Затем код копирует из потока файлов в поток вложений и выпускает оба потока.
  
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


