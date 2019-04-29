---
title: Управление сообщениями в OST без вызова синхронизации в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Содержит пример кода на языке C++, который показывает, как использовать Иид_имессажерав в IMsgStore:: OpenEntry, чтобы получить интерфейс IMessage, который управляет сообщением в файле автономных папок (OST) без принудительного скачивания всего сообщения, когда клиент находится в кэшированной среде Exchange Режимов.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418759"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Управление сообщениями в OST без вызова синхронизации в режиме кэширования Exchange

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе приведен пример кода на языке C++, который показывает, `IID_IMessageRaw` как использовать в **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** , чтобы получить интерфейс **[iMessage](imessageimapiprop.md)** , который управляет сообщением в файле автономных папок (OST) без принудительного скачивания всего сообщения, когда клиент находится в режиме кэширования Exchange. 
  
Когда клиент находится в режиме кэширования Exchange, сообщения в OST могут находиться в одном из двух состояний:
  
- Загружаются все сообщения, содержащие заголовок и текст сообщения.
    
- Загружается сообщение с только заголовком.
    
Когда вы запрашиваете интерфейс **iMessage** для сообщения в OST-файле и клиент находится в режиме кэширования Exchange, `IID_IMessageRaw`используйте. Если вы `IID_IMessage` запрашиваете интерфейс **iMessage** , и если сообщение содержит только заголовок, загруженный в OST, вы вызываете синхронизацию, которая пытается скачать все сообщение. 
  
Если вы используете `IID_IMessageRaw` или `IID_IMessage` запрашиваете интерфейс **iMessage** , возвращаемые интерфейсы идентичны. Интерфейс **iMessage** , который был запрошен с помощью `IID_IMessageRaw` метода, возвращает сообщение электронной почты в том виде, в котором оно существует в OST, и синхронизация не выполняется принудительно. 
  
В приведенном ниже примере показано, как вызвать метод **OpenEntry** , `IID_IMessageRaw` передав вместо `IID_IMessage`него.
  
```cpp
HRESULT HrOpenRawMessage ( 
    LPMDB lpMSB,  
    ULONG cbEntryID,  
    LPENTRYID lpEntryID,  
    ULONG ulFlags,  
    LPMESSAGE* lpMessage) 
{ 
    ULONG ulObjType = NULL; 
 
    HRESULT hRes = lpMDB->OpenEntry( 
        cbEntryID, 
        lpEntryID, 
        IID_IMessageRaw, 
        ulFlags, 
        &ulObjType, 
        (LPUNKNOWN*) lpMessage)); 
 
   return hRes; 
} 

```

Если метод **OpenEntry** возвращает код ошибки **мапи_е_интерфаце_нот_суппортед** , он указывает на то, что хранилище сообщений не поддерживает доступ к сообщению в режиме RAW. В этом случае повторите метод **OpenEntry** , передав `IID_IMessage`значение.

> [!IMPORTANT]
>  `IID_IMessageRaw`не может быть определен в файле заголовков, которые есть у вас в данный момент. В этом случае можно добавить его в код с помощью следующего определения. Используйте макрос ДЕФИНЕ_ОЛЕГУИД, определенный в файле заголовка пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) guiddef. h, чтобы связать символьное имя GUID со значением. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

