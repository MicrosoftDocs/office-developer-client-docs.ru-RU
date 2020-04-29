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
  
Открытие вложения подразумевает отображение его данных. Например, при открытии вложения файла отображается его содержимое. В то время как сообщения и папки открываются с помощью идентификаторов записей, вложения открываются с использованием их номеров вложений — **PR_ATTACH_NUM** свойства. Дополнительные сведения см **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)). Номера вложений доступны в таблице вложений сообщения.
  
### <a name="to-open-all-attachments-in-a-message"></a>Открытие всех вложений в сообщении
  
1. Вызовите метод сообщения [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) для доступа к своей таблице вложений. 
    
2. Вызовите [хркуеряллровс](hrqueryallrows.md) для получения всех строк в таблице. 
    
3. Для каждой строки: 
    
    1. Откройте вложение, передав номер вложения, представленный в столбце **PR_ATTACH_NUM** , в вызове метода **iMessage:: опенаттач** сообщения. Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md). **Опенаттач** возвращает указатель на реализацию **иаттач** , которая предоставляет доступ к свойствам вложений. 
        
    2. Вызовите метод **IMAPIProp::/PROPS** вложения для получения свойства **PR_ATTACH_METHOD** . Дополнительные сведения см. в статье [IMAPIProp::-PROPS](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)).
        
    3. Если для **PR_ATTACH_METHOD** задано значение ATTACH_BY_REF_ONLY, вызовите метод **IMAPIProp::-PROPS** для получения свойства **PR_ATTACH_PATHNAME** . Дополнительные сведения см **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)).
        
    4. Если для параметра **PR\_ATTACH_METHOD** задано\_присоединение BY_VALUE, вызовите метод **IMAPIProp:: опенпроперти** , чтобы открыть свойство **\_PR ATTACH_DATA_BIN** с помощью интерфейса **IStream** . Ниже приведен пример кода, приведенного в этом разделе. Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).
        
    5. Если для параметра **PR_ATTACH_METHOD** задано значение ATTACH_OLE, а вложение является объектом OLE 2: 
        
        1. Call **IMAPIProp:: опенпроперти** для открытия свойства **PR\_ATTACH_DATA_OBJ** с помощью интерфейса **помощью istreamdocfile** . Попытаться использовать этот интерфейс, так как это реализация **IStream** обеспечивает работу с структурированным хранилищем с минимальным количеством издержек. Дополнительные сведения см **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)).
            
        2. Если произошел сбой вызова **опенпроперти** , повторно вызовите его для получения свойства **PR_ATTACH_DATA_BIN** с помощью интерфейса **помощью istreamdocfile** . 
            
        3. Если второй вызов **опенпроперти** завершается с ошибкой, попробуйте вызвать **опенпроперти** для получения **PR_ATTACH_DATA_OBJ**. Однако вместо параметра **помощью istreamdocfile**укажите интерфейс **IStorage** . 
    
4. Если для **PR_ATTACH_METHOD** задано значение ATTACH_EMBEDDED_MSG, нередко используется значение **PR_ATTACH_DATA_OBJ** для хранения ошибки. Это связано с тем, что у вас и у средства реализации таблиц нет способа согласовать тип возвращаемого объекта. Чтобы получить указатель на вложенное сообщение, откройте вложение с помощью **iMessage:: опенаттач**. Затем можно получить доступ к данным вложения, вызвав метод **IMAPIProp:: опенпроперти** . Дополнительные сведения см. в статье [iMessage:: опенаттач](imessage-openattach.md) and [IMAPIProp:: опенпроперти](imapiprop-openproperty.md).
    
Вы можете запросить открытие вложения в режиме чтения и записи или только для чтения. Режим "только чтение" используется по умолчанию, а многие поставщики хранилищ сообщений открывают все вложения в этом режиме независимо от того, какие клиенты запрашивают запрос. Передайте флаг MAPI_BEST_ACCESS, чтобы запросить предоставление поставщиком хранилища сообщений максимального уровня доступа, а затем извлеките свойство **PR_ACCESS_LEVEL** открытого вложения, чтобы определить уровень доступа, который фактически предоставлен. Дополнительные сведения см **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
В приведенном ниже примере показано, как открыть данные в свойстве **PR\_вложения ATTACH_DATA_BIN** . Он выделяет указатели на два потока: один для файла и один для вложения. Функция **опенстреамонфиле** открывает поток файлов в режиме "только для чтения". Вызов метода вложения **IMAPIProp:: опенпроперти** открывает поток вложений в режиме чтения и записи. Дополнительные сведения см **PR_ATTACH_DATA_BIN**, [опенстреамонфиле](openstreamonfile.md)и [IMAPIProp:: опенпроперти](imapiprop-openproperty.md). Затем код копирует из потока файлов в поток вложений и освобождает оба потока.
  
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


