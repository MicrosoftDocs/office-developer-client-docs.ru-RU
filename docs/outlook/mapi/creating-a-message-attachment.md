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
ms.openlocfilehash: 34d8dbeaf101d5ebb687403a2200bd0ad73b9998
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577102"
---
# <a name="creating-a-message-attachment"></a>Создание вложения к сообщению
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вложения сообщения является некоторые дополнительные данные, такие как файл, другое сообщение или OLE-объект, который вы можете отправить или сохранить, а также сообщение. Каждый вложение содержит набор свойств, определяющий ее, а также его тип и порядок отображения. Как получатели вложений сообщений осуществляется только по почте, к которым они относятся. Таким образом вложения для использования в его сообщение необходимо открыть.
  
## <a name="create-a-message-attachment"></a>Создание вложения сообщения
  
1. Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) сообщений и передать значение NULL в качестве идентификатора интерфейса. **CreateAttach** возвращает число, однозначно идентифицирующее новые вложения в сообщение. Число вложений хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) и действителен только, пока открыта сообщение, содержащее вложение.
    
2. Вызовите [IMAPIProp::SetProps](imapiprop-setprops.md) , чтобы задать **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) для указания того, как получить доступ к вложение. **PR_ATTACH_METHOD** является обязательным. Значение: 
    
   - ATTACH_BY_VALUE, если вложение двоичных данных.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение представляет собой файл.
    
   - ATTACH_EMBEDDED_MSG, если сообщение имеет вложение.
    
   - ATTACH_OLE, если вложение является объектом OLE.
    
3. Задайте для свойства данных соответствующих вложений:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) для двоичных данных и объекты OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) для файлов.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) для сообщений и объекты OLE 2.
    
4. Задайте **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) для хранения графического представления вложения для файла или двоичные вложения. Не устанавливайте его, объекты OLE, хранящих сведения о визуализации во внутренней сети, или вложенные сообщений. 
    
5. Задайте **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) для указания, где должны отображаться вложение. **PR_RENDERING_POSITION** применяется только к клиентам, которые необходимо задать свойство **PR_BODY** . Если вы поддерживаете только **PR_RTF_COMPRESSED**, поместите со следующими сведениями заполнитель в сжатый поток:
    
   `\objattph`

   Чтобы задать **PR_RENDERING_POSITION**, назначьте либо число, представляющее порядковый номер сдвиг знака с первым символом **PR_BODY** , 0, если вам нужно знать, где в сообщение, отображаемое вложения или 0xFFFFFFFF, если он не задан Отображать вложения в **PR_BODY**.
    
6. Установка **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) для указания краткое имя файла для файла вложения и **связей с Общественностью\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) для указания имени файла, как поддерживаются на платформе, обрабатывающего формат длинное имя файла. Оба свойства являются необязательными. Тем не менее если значение **PR_ATTACH_LONG_FILENAME**, также необходимо задайте **PR_ATTACH_FILENAME**. 
    
7. Задайте **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) для указания имени для вложения, которые отображаются в диалоговом окне. PR_DISPLAY_NAME не является обязательным. 
    
## <a name="set-prattachdatabin"></a>Набор PR_ATTACH_DATA_BIN
  
1. Вызовите [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть свойства с помощью интерфейса **IStream** . 
    
2. Если файл содержит данные и откроется или требуется явных контролировать размер буфера, вызовите **IStream::Write** в цикле для помещения данных в поток. 
    
3. Другая возможность — это вызов **OpenStreamOnFile** для создания потока для доступа к файлу данных и затем вызвать метод **IStream::CopyTo** этот поток для копирования данных в поток, возвращенный **OpenProperty**.
    
4. Вызов метода **IStream::Commit** нового потока. 
    
## <a name="set-prattachdataobj"></a>Набор PR_ATTACH_DATA_OBJ
  
1. Вызовите **IMAPIProp::OpenProperty** , чтобы открыть свойства с помощью интерфейса **IStreamDocfile** для создания потока, который работает с структурированного хранилища. **IStreamDocfile** реализуется поставщиками хранилища сообщений для предоставления клиентам возможности более высокую производительность для хранения и извлечения структурированного хранилища. Интерфейс **IStreamDocfile** совпадает с **IStream**, но содержимое потока гарантированно быть в формате структурированного хранилища. Если этот вызов выполняется успешно, создайте потока с те же действия, описанные для настройки **PR_ATTACH_DATA_BIN**.
    
2. В случае сбоя **OpenProperty** : 
    
   1. Вызов еще раз запросом для **IStorage** **OpenProperty** . 
      
   2. Вызов **StgOpenStorage** для открытия объекта OLE и возвращает объект хранилища. 
      
   3. Вызов метода **IStorage::CopyTo** объекта возвращенные хранилища для копирования объекта хранилища, возвращенные **OpenProperty**.
      
   4. Вызов метода **IStorage::Commit** новый объект хранилища. 
    
## <a name="set-prattachpathname"></a>Набор PR_ATTACH_PATHNAME
  
1. Выделить структуру [SPropValue](spropvalue.md) , установка для члена **ulPropTag** **PR_ATTACH_PATHNAME** и член **Value.LPSZ** к строке, которая представляет имя файла. 
    
2. Вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) вложения. 
    
> [!NOTE]
> Если система поддерживает длинные имена файлов, необходимо задайте **PR_ATTACH_PATHNAME** и **PR_ATTACH_LONG_PATHNAME**. Может потребоваться внести без системы звонок, чтобы получить короткое имя файла. 
  
## <a name="see-also"></a>См. также

- [�������� MAPI](mapi-attachments.md)

