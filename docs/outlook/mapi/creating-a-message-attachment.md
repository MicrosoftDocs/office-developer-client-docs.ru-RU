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
  
Вложение сообщения — это некоторые дополнительные данные, например файл, другое сообщение или объект OLE, которые можно отправлять и сохранять вместе с сообщением. Каждое вложение имеет коллекцию свойств, определяющих его и описывающую его тип и способ отображения. Как и получатели, доступ к вложениям сообщений возможен только через сообщение, к которому они относятся. Таким образом, чтобы вложение можно было использовать, его сообщение должно быть открыто.
  
## <a name="create-a-message-attachment"></a>Создание вложения сообщения
  
1. Вызовите метод сообщения [iMessage:: креатеаттач](imessage-createattach.md) и передайте значение NULL в качестве идентификатора интерфейса. **Креатеаттач** возвращает число, которое уникально идентифицирует новое вложение в сообщении. Номер вложения хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) и действителен только до тех пор, пока не будет открыто сообщение, содержащее вложение.
    
2. Call [IMAPIProp:: SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)), чтобы указать, как получить доступ к вложению. **PR_ATTACH_METHOD** является обязательным. Задайте для него значение: 
    
   - ATTACH_BY_VALUE, если вложение двоичные данные.
    
   - ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE или ATTACH_BY_REF_ONLY, если вложение является файлом.
    
   - ATTACH_EMBEDDED_MSG, если вложение является сообщением.
    
   - ATTACH_OLE, если вложение является объектом OLE.
    
3. Задайте соответствующее свойство данных вложения:
    
   - **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) для двоичных данных и объектов OLE 1.
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) для файлов.
    
   - **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) для сообщений и объектов OLE 2.
    
4. Задайте **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)), чтобы сохранить графическое представление вложения для файла или двоичных вложений. Не задавайте его для объектов OLE, которые хранят данные отображения для внутреннего использования или для вложенных сообщений. 
    
5. Задайте **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)), чтобы указать, где должно отображаться вложение. **PR_RENDERING_POSITION** применяется только к клиентам, которые задают свойство **PR_BODY** . Если вы поддерживаете **PR_RTF_COMPRESSED**, вставьте в сжатый поток следующие сведения о заполнителе:
    
   `\objattph`

   Чтобы задать **PR_RENDERING_POSITION**, назначьте число, представляющее порядковое смещение в символах, с первым символом **PR_BODY** равно 0, если вам нужно знать, где в сообщении отображается вложение, или 0xFFFFFFFF, если вы не отрисовываете вложения в **PR_BODY**.
    
6. Задайте **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)), чтобы указать краткое имя файла для вложенного файла и **ATTACH_LONG_FILENAME\_PR** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)), чтобы указать имя файла, которое поддерживается на платформе, которая обрабатывает формат длинного имени файла. Оба свойства являются необязательными. Тем не менее, если вы настроили **PR_ATTACH_LONG_FILENAME**, также установите **PR_ATTACH_FILENAME**. 
    
7. Задайте **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), чтобы указать имя вложения, которое может отображаться в диалоговом окне. PR_DISPLAY_NAME не является обязательным. 
    
## <a name="set-pr_attach_data_bin"></a>Настройка PR_ATTACH_DATA_BIN
  
1. Call [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство с помощью интерфейса **IStream** . 
    
2. Если файл содержит данные, который открыт, или если требуется явный контроль над размером буфера, вызовите **IStream:: Write** в цикле, чтобы поместить данные в поток. 
    
3. Кроме того, можно вызвать **опенстреамонфиле** , чтобы создать поток для доступа к файлу данных, а затем вызвать метод **IStream:: CopyTo** для копирования данных в поток, возвращенный методом **опенпроперти**.
    
4. Вызовите метод **IStream:: Commit** нового потока. 
    
## <a name="set-pr_attach_data_obj"></a>Настройка PR_ATTACH_DATA_OBJ
  
1. Call **IMAPIProp:: опенпроперти** , чтобы открыть свойство с помощью интерфейса **помощью istreamdocfile** , чтобы создать поток, работающий с структурированным хранилищем. **Помощью istreamdocfile** реализуется поставщиками хранилищ сообщений для предоставления клиентам более производительного способа хранения и извлечения структурированного хранилища. Интерфейс **помощью istreamdocfile** аналогичен интерфейсу **IStream**, но содержимое потока гарантированно форматируется как структурированное хранилище. При успешном выполнении этого вызова создайте поток с теми же действиями, что и для настройки **PR_ATTACH_DATA_BIN**.
    
2. Если **опенпроперти** не удастся: 
    
   1. Снова вызовите **опенпроперти** для запроса **IStorage**. 
      
   2. Вызовите **стгопенстораже** , чтобы открыть объект OLE и возвратить объект Storage. 
      
   3. Вызовите возвращенный объект **IStorage:: CopyTo** для копирования в объект хранилища, возвращенный из **опенпроперти**.
      
   4. Вызовите метод **IStorage: Commit нового объекта Storage:: Commit** . 
    
## <a name="set-pr_attach_pathname"></a>Настройка PR_ATTACH_PATHNAME
  
1. Выделите структуру [спропвалуе](spropvalue.md) , задав для члена **улпроптаг** значение **PR_ATTACH_PATHNAME** и элемент **value. лпсз** в строку символов, представляющую имя файла. 
    
2. Вызовите метод вложения [IMAPIProp:: SetProps](imapiprop-setprops.md) . 
    
> [!NOTE]
> Если ваша платформа поддерживает длинные имена файлов, установите как **PR_ATTACH_PATHNAME** , так и **PR_ATTACH_LONG_PATHNAME**. Может потребоваться вызов операционной системы для получения короткого имени файла. 
  
## <a name="see-also"></a>См. также

- [Вложения MAPI](mapi-attachments.md)

