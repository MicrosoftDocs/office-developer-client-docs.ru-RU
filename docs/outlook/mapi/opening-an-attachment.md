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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Открытие вложения включает отображение его данных. Например, при открытом вложении файла отображается его содержимое. В то время как сообщения и папки открываются с использованием идентификаторов записей, вложения открываются с помощью номеров PR_ATTACH_NUM **свойств.** Дополнительные сведения **см. в PR_ATTACH_NUM** ([PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) Номера вложений доступны в таблице вложений сообщения.
  
### <a name="to-open-all-attachments-in-a-message"></a>Открытие всех вложений в сообщении
  
1. Вызовите метод [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) сообщения, чтобы получить доступ к таблице вложений. 
    
2. Вызовите [HrQueryAllRows,](hrqueryallrows.md) чтобы получить все строки в таблице. 
    
3. Для каждой строки: 
    
    1. Откройте вложение, передав номер вложения, **представленный** в столбце PR_ATTACH_NUM в вызове метода **IMessage::OpenAttach** сообщения. Дополнительные сведения см. в [IMessage::OpenAttach.](imessage-openattach.md) **OpenAttach** возвращает указатель на реализацию **IAttach,** которая предоставляет доступ к свойствам вложения. 
        
    2. Вызовите метод **IMAPIProp::GetProps** вложения, чтобы получить **его PR_ATTACH_METHOD.** Дополнительные сведения см. в подразделе [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod).](pidtagattachmethod-canonical-property.md)
        
    3. Если **PR_ATTACH_METHOD** установлено ATTACH_BY_REF_ONLY, вызовите **IMAPIProp::GetProps,** чтобы **получить PR_ATTACH_PATHNAME** свойства. Дополнительные сведения **см. в PR_ATTACH_PATHNAME** ([PidTagAttachPathname).](pidtagattachpathname-canonical-property.md)
        
    4. Если **\_ для ATTACH_METHOD** pr установлено значение ATTACH BY_VALUE, вызовите \_ **IMAPIProp::OpenProperty,** чтобы открыть свойство **PR \_** ATTACH_DATA_BIN с помощью **интерфейса IStream.** См. пример кода, следующего за этой процедурой. Дополнительные сведения см. в подразделе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary).](pidtagattachdatabinary-canonical-property.md)
        
    5. Если **PR_ATTACH_METHOD** установлено ATTACH_OLE и вложением является объект OLE 2: 
        
        1. Вызовите **IMAPIProp::OpenProperty,** чтобы открыть **ATTACH_DATA_OBJ PR \_** с помощью интерфейса **IStreamDocfile.** Старайтесь использовать этот интерфейс, так как это реализация **IStream,** гарантируемая для работы со структурированным хранилищем с наименьшим объемом дополнительных расходов. Дополнительные сведения **см. в PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject).](pidtagattachdataobject-canonical-property.md)
            
        2. Если вызов **OpenProperty** не удается, вызовите  его еще раз, чтобы получить PR_ATTACH_DATA_BIN с интерфейсом **IStreamDocfile.** 
            
        3. Если второй вызов **OpenProperty** не удается, попробуйте еще раз вызвать **OpenProperty,** чтобы **PR_ATTACH_DATA_OBJ**. Однако вместо указания **IStreamDocfile** укажите **интерфейс IStorage.** 
    
4. Если **PR_ATTACH_METHOD** установлено значение ATTACH_EMBEDDED_MSG, значение PR_ATTACH_DATA_OBJ содержать ошибку.  Это происходит потому, что вы и реализутель таблицы не можете согласовать тип возвращаемого объекта. Чтобы получить указатель на вложенное сообщение, откройте вложение с помощью **IMessage::OpenAttach.** Затем для доступа к данным вложения вызывается метод **IMAPIProp::OpenProperty.** Дополнительные сведения см. в подразделах [IMessage::OpenAttach](imessage-openattach.md) и [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)
    
Вы можете запросить открытие вложения в режиме чтения,записи или только для чтения. Режим "только чтение" является режимом по умолчанию, и многие поставщики хранимых сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают. Передай флаг MAPI_BEST_ACCESS, чтобы попросить поставщика магазина сообщений предоставить ему самый высокий уровень доступа, а затем получить свойство PR_ACCESS_LEVEL открытого вложения, чтобы определить фактически предоставленный уровень доступа.  Дополнительные сведения **см. в PR_ACCESS_LEVEL** ([PidTagAccessLevel).](pidtagaccesslevel-canonical-property.md)
  
В следующем примере показано, как открыть данные в свойстве **PR \_ ATTACH_DATA_BIN вложения.** Он выделяет указатели двум потокам: одному для файла и одному для вложения. Функция **OpenStreamOnFile** открывает поток файлов в режиме только для чтения. Вызов метода **IMAPIProp::OpenProperty** вложения открывает поток вложений в режиме чтения и записи. Дополнительные сведения **см. в PR_ATTACH_DATA_BIN,** [OpenStreamOnFile](openstreamonfile.md)и [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Затем код копирует из потока файлов в поток вложений и освобождает оба потока.
  
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


