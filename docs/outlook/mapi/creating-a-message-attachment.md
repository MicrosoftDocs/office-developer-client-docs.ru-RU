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
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вложение сообщения — это дополнительные данные, такие как файл, другое сообщение или объект OLE, которые можно отправить или сохранить вместе с сообщением. Каждое вложение имеет коллекцию свойств, которые идентифицируют его и описывают его тип и его отрисовку. Как и получатели, к вложениям сообщений можно получить доступ только через сообщение, к которому они принадлежат. Поэтому для того, чтобы вложение можно было использовать, его сообщение должно быть открытым.
  
## <a name="create-a-message-attachment"></a>Создание вложения сообщения
  
1. Вызовите метод [IMessage::CreateAttach](imessage-createattach.md) и передайте NULL в качестве идентификатора интерфейса. **CreateAttach** возвращает номер, уникальный для идентификации нового вложения в сообщении. Номер вложения хранится в **свойстве** [PR_ATTACH_NUM (PidTagAttachNumber)](pidtagattachnumber-canonical-property.md)и действителен до тех пор, пока сообщение, содержащее вложение, будет открыто.
    
2. Позвоните [в IMAPIProp::SetProps](imapiprop-setprops.md) **для** PR_ATTACH_METHOD [(PidTagAttachMethod),](pidtagattachmethod-canonical-property.md)чтобы указать, как получить доступ к вложению. **PR_ATTACH_METHOD** требуется. Установите его на: 
    
   - ATTACH_BY_VALUE, если вложение является двоичными данными.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение — это файл.
    
   - ATTACH_EMBEDDED_MSG, если вложение является сообщением.
    
   - ATTACH_OLE если вложение является объектом OLE.
    
3. Установите соответствующее свойство данных вложения:
    
   - **PR_ATTACH_DATA_BIN** [(PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)для двоичных данных и объектов OLE 1.
    
   - **PR_ATTACH_PATHNAME** [(PidTagAttachPathname)](pidtagattachpathname-canonical-property.md)для файлов.
    
   - **PR_ATTACH_DATA_OBJ** [(PidTagAttachDataObject)](pidtagattachdataobject-canonical-property.md)для сообщений и объектов OLE 2.
    
4. Установите **PR_ATTACH_RENDERING** [(PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)для удержания графического представления вложения для файлов или двоичных вложений. Не установите его для объектов OLE, которые хранят сведения о отрисовке внутри страны, или для присоединенных сообщений. 
    
5. Установите **PR_RENDERING_POSITION** [(PidTagRenderingPosition),](pidtagrenderingposition-canonical-property.md)чтобы указать, где должно отображаться вложение. **PR_RENDERING_POSITION** применяется только к клиентам, которые  PR_BODY свойству. Если вы поддерживаете **только PR_RTF_COMPRESSED,** поместите в сжатый поток следующие сведения о месте.
    
   `\objattph`

   Чтобы задать **PR_RENDERING_POSITION,** назначьте либо номер, который представляет ordinal offset в символах, с первым персонажем **PR_BODY** быть 0, если вам нужно знать, где в сообщении отрисовка вложения, или 0xFFFFFFFF, если вы не отрисовки вложений в **PR_BODY**.
    
6. Установите **PR_ATTACH_FILENAME** [(PidTagAttachFilename),](pidtagattachfilename-canonical-property.md)чтобы указать короткое имя файла для вложения файлов и PR **\_ ATTACH_LONG_FILENAME** [(PidTagAttachLongFilename),](pidtagattachlongfilename-canonical-property.md)чтобы указать имя файла, поддерживаемого на платформе, которая обрабатывает длинный формат имен файлов. Оба свойства необязательны. Однако, если вы **PR_ATTACH_LONG_FILENAME,** также установите **PR_ATTACH_FILENAME**. 
    
7. Установите **PR_DISPLAY_NAME** [(PidTagDisplayName),](pidtagdisplayname-canonical-property.md)чтобы указать имя вложения, которое может отображаться в диалоговом окне. PR_DISPLAY_NAME необязательный. 
    
## <a name="set-pr_attach_data_bin"></a>Настройка PR_ATTACH_DATA_BIN
  
1. Вызов [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство с интерфейсом **IStream.** 
    
2. Если файл содержит данные и он открыт или требуется явный контроль над размером буфера, позвоните **в IStream::Write** в цикле, чтобы разместить данные в потоке. 
    
3. Другой вариант — вызвать **OpenStreamOnFile,** чтобы создать поток для доступа к файлу данных, а затем вызвать метод **IStream::CopyTo** этого потока, чтобы скопировать данные в поток, возвращенный **OpenProperty.**
    
4. Вызов метода **IStream::Commit** нового потока. 
    
## <a name="set-pr_attach_data_obj"></a>Настройка PR_ATTACH_DATA_OBJ
  
1. Вызов **IMAPIProp::OpenProperty,** чтобы открыть свойство с помощью **интерфейса IStreamDocfile,** чтобы создать поток, который работает со структурированным хранилищем. **IStreamDocfile** реализуется поставщиками хранилища сообщений, чтобы предоставить клиентам более высокой производительности хранение и извлечение структурированного хранилища. Интерфейс **IStreamDocfile** такой же, как **iStream,** но содержимое потока гарантированно будет отформатироваться как структурированное хранилище. Если этот вызов удался, создайте поток с помощью тех же действий, что и **для PR_ATTACH_DATA_BIN.**
    
2. Если **сбой OpenProperty:** 
    
   1. Снова **вызывай OpenProperty** с просьбой **о IStorage.** 
      
   2. Вызов **StgOpenStorage,** чтобы открыть объект OLE и вернуть объект хранения. 
      
   3. Вызывай метод **IStorage::CopyTo** возвращаемого объекта хранения, чтобы скопировать объект хранения, возвращенный **из OpenProperty.**
      
   4. Вызов метода **IStorage::Commit нового** объекта хранения. 
    
## <a name="set-pr_attach_pathname"></a>Настройка PR_ATTACH_PATHNAME
  
1. Распределите [структуру SPropValue,](spropvalue.md) **установив** для члена **ulPropTag** значение PR_ATTACH_PATHNAME и члена **Value.LPSZ** в строку символов, представляюую имя файла. 
    
2. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) в приложении. 
    
> [!NOTE]
> Если платформа поддерживает длинные имена файлов, установите PR_ATTACH_PATHNAME **и PR_ATTACH_LONG_PATHNAME.**  Может потребоваться вызвать операционную систему, чтобы получить короткое имя файла. 
  
## <a name="see-also"></a>См. также

- [Вложения MAPI](mapi-attachments.md)

