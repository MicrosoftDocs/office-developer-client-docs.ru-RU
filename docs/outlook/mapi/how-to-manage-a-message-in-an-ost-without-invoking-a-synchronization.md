---
title: Управление сообщениями в OST без ссылки на синхронизацию в режиме кэширования Exchange.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Содержит пример кода в C++, который показывает, как использовать IID_IMessageRaw в IMsgStore::OpenEntry для получения интерфейса IMessage, который управляет сообщением в файле автономных папок (OST), не принуждая скачивать все сообщение, когда клиент находится в кэшировать Exchange Mode.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418759"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Управление сообщениями в OST без ссылки на синхронизацию в режиме кэширования Exchange.

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример кода в C++, который показывает, как использовать `IID_IMessageRaw` **[в IMsgStore::OpenEntry](imsgstore-openentry.md)** для получения интерфейса **[IMessage,](imessageimapiprop.md)** который управляет сообщением в файле автономных папок (OST), не принуждая скачивать все сообщение, когда клиент находится в кэшировать Exchange Mode. 
  
Когда клиент находится в режиме кэш Exchange, сообщения в OST могут быть в одном из двух штатов:
  
- Скачано все сообщение, содержаное заголовка и тело.
    
- Скачивается сообщение с только загонами.
    
При запросе **интерфейса IMessage** для сообщения в OST и клиент находится в режиме кэш Exchange, используйте `IID_IMessageRaw` . Если вы используете для запроса  `IID_IMessage` **интерфейса IMessage** и если в сообщении есть только его загон, загруженный в OST, вы вызываете синхронизацию, которая пытается скачать все сообщение. 
  
При использовании  `IID_IMessageRaw` или  `IID_IMessage` запросе **интерфейса IMessage** возвращенные интерфейсы идентичны по использованию. Интерфейс **IMessage,** который был запрошен с помощью возвращает сообщение электронной почты, так как оно существует в OST, и синхронизация  `IID_IMessageRaw` не является принудительной. 
  
В следующем примере показано, как вызвать метод **OpenEntry,** передав  `IID_IMessageRaw` вместо  `IID_IMessage` .
  
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

Если метод **OpenEntry** возвращает  код ошибки MAPI_E_INTERFACE_NOT_SUPPORTED, он указывает, что хранилище сообщений не поддерживает доступ к сообщению в сыром режиме. В этой ситуации попробуйте метод **OpenEntry** еще раз, передав  `IID_IMessage` .

> [!IMPORTANT]
>  `IID_IMessageRaw` может быть не определено в загружаемом файле загона, который у вас есть в настоящее время. В этом случае вы можете добавить его в код с помощью следующего определения. Используйте макрос DEFINE_OLEGUID, определенный в файле guiddef.h Windows набора разработки программного обеспечения (SDK), чтобы связать символическое имя GUID с его значением. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

