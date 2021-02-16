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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405998"
---
# <a name="creating-a-message-attachment"></a>Создание вложения к сообщению
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вложение сообщения — это некоторые дополнительные данные, такие как файл, другое сообщение или объект OLE, которые можно отправить или сохранить вместе с сообщением. Каждое вложение имеет коллекцию свойств, идентифицирует его и описывает его тип и его отрисовку. Как и для получателей, доступ к вложениям сообщений можно получить только через сообщение, к которому они принадлежат. Следовательно, чтобы вложение можно было использовать, его сообщение должно быть открыто.
  
## <a name="create-a-message-attachment"></a>Создание вложения сообщения
  
1. Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) сообщения и передайте NULL в качестве идентификатора интерфейса. **CreateAttach** возвращает номер, однозначно определяя новое вложение в сообщении. Номер вложения хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)и действителен, только если открыто сообщение с вложением.
    
2. Вызовите [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы PR_ATTACH_METHOD ([PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)чтобы указать, как получить доступ к вложение.  **PR_ATTACH_METHOD** требуется. Установите для него 24-е. 
    
   - ATTACH_BY_VALUE, является ли вложение двоичными данными.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение является файлом.
    
   - ATTACH_EMBEDDED_MSG, является ли вложение сообщением.
    
   - ATTACH_OLE, если вложение является объектом OLE.
    
3. Установите соответствующее свойство данных вложения:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)для двоичных данных и объектов OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)для файлов.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)для сообщений и объектов OLE 2.
    
4. **Задайте PR_ATTACH_RENDERING** ([PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)для удержания графического представления вложения для файлов или двоичных вложений. Не устанавливать его для объектов OLE, в которых хранятся сведения об отрисовке внутри организации или для вложенных сообщений. 
    
5. Зада **PR_RENDERING_POSITION** ([PidTagRenderingPosition),](pidtagrenderingposition-canonical-property.md)чтобы указать, где должно отображаться вложение. **PR_RENDERING_POSITION** применяется только к клиентам, которые PR_BODY **свойства.** Если вы поддерживаете только **PR_RTF_COMPRESSED,** поместите в сжатый поток следующие данные-замессыщики:
    
   `\objattph`

   Чтобы задать **PR_RENDERING_POSITION,** назначьте либо число, которое представляет порядковую смещение символов, с первым символом **PR_BODY** 0, если вам нужно знать, где в сообщении отрисовка вложения, или 0xFFFFFFFF, если не отрисовка вложений в PR_BODY **.**
    
6. Установите **PR_ATTACH_FILENAME** ([PidTagAttachFilename),](pidtagattachfilename-canonical-property.md)чтобы указать короткое имя файла для вложенного файла и **PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename),](pidtagattachlongfilename-canonical-property.md)чтобы указать имя файла, поддерживаемого на платформе, которая обрабатывает длинный формат имени файла. Оба свойства являются необязательными. Однако, если вы **PR_ATTACH_LONG_FILENAME,** также **установите** PR_ATTACH_FILENAME . 
    
7. **Задайте PR_DISPLAY_NAME** ([PidTagDisplayName),](pidtagdisplayname-canonical-property.md)чтобы указать имя вложения, которое может отображаться в диалоговом окне. PR_DISPLAY_NAME необязательный. 
    
## <a name="set-pr_attach_data_bin"></a>Настройка PR_ATTACH_DATA_BIN
  
1. Вызовите [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство с помощью **интерфейса IStream.** 
    
2. Если файл содержит данные и он открыт или требуется явный контроль над размером буфера, вызовите **IStream::Write** в цикле, чтобы разместить данные в потоке. 
    
3. Другой вариант — вызвать **OpenStreamOnFile,** чтобы создать поток для доступа к файлу данных, а затем вызвать метод **IStream::CopyTo** этого потока, чтобы скопировать данные в поток, возвращенный **OpenProperty.**
    
4. Вызовите метод **IStream::Commit** нового потока. 
    
## <a name="set-pr_attach_data_obj"></a>Настройка PR_ATTACH_DATA_OBJ
  
1. Вызовите **IMAPIProp::OpenProperty,** чтобы открыть свойство с помощью интерфейса **IStreamDocfile,** чтобы создать поток, который работает со структурированным хранилищем. **IStreamDocfile** реализуется поставщиками хранилища сообщений, чтобы предоставить клиентам более высокий способ хранения и извлечения структурированного хранилища. Интерфейс **IStreamDocfile** такой же, как **IStream,** но содержимое потока гарантированно будет отформатировано как структурированное хранилище. Если этот вызов будет успешным, создайте поток, выполив те же действия, что и **PR_ATTACH_DATA_BIN.**
    
2. Если **сбой OpenProperty:** 
    
   1. Снова **вызовите OpenProperty** с запросом **IStorage.** 
      
   2. Вызовите **StgOpenStorage,** чтобы открыть объект OLE и вернуть объект хранилища. 
      
   3. Вызовите метод **IStorage::CopyTo** возвращенного объекта хранилища, чтобы скопировать его в объект хранилища, возвращенный **из OpenProperty.**
      
   4. Вызовите метод **IStorage::Commit** нового объекта хранилища. 
    
## <a name="set-pr_attach_pathname"></a>Настройка PR_ATTACH_PATHNAME
  
1. Выделите структуру [SPropValue,](spropvalue.md) установив для члена **ulPropTag** значение **PR_ATTACH_PATHNAME,** а для параметра **Value.LPSZ** строку символов, которая представляет имя файла. 
    
2. Вызовите метод [IMAPIProp::SetProps вложения.](imapiprop-setprops.md) 
    
> [!NOTE]
> Если платформа поддерживает длинные имена файлов, установите и **PR_ATTACH_PATHNAME,** и **PR_ATTACH_LONG_PATHNAME.** Для получения короткого имени файла может потребоваться вызов операционной системы. 
  
## <a name="see-also"></a>См. также

- [MAPI Attachments](mapi-attachments.md)

