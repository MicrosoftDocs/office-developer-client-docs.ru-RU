---
title: Управление сообщениями в OST без вызова синхронизации в режиме кэширования данных Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Содержит пример кода на C++, в котором показано, как использовать IID_IMessageRaw в IMsgStore::OpenEntry для получения IMessage интерфейса, который управляет сообщения в файле автономной папки (OST) без перезагрузки на загрузку сообщений целиком, если клиентом является в кэширования данных Exchange Режим.
ms.openlocfilehash: e32bf4f64bfb91979133ee983e45481b3d5b9732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808625"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a>Управление сообщениями в OST без вызова синхронизации в режиме кэширования данных Exchange

**Относится к**: Outlook 
  
В этом разделе содержится пример кода на C++, в котором показано, как использовать `IID_IMessageRaw` в **[IMsgStore::OpenEntry](imsgstore-openentry.md)** для получения **[IMessage](imessageimapiprop.md)** интерфейса, который управляет сообщения в файле автономной папки (OST) без перезагрузки загрузки всей сообщение клиента работает в режиме кэширования данных Exchange. 
  
Если клиент входит в режиме кэширования Exchange, сообщения в OST может быть в одном из двух режимов:
  
- Загрузить целиком сообщения, содержащего заголовок и тело.
    
- Загрузить сообщение с только его заголовок.
    
Когда запросить интерфейс **IMessage** сообщения в автономной папки и клиент — в режиме кэширования Exchange, используйте `IID_IMessageRaw`. Если вы используете `IID_IMessage` для запроса **IMessage** интерфейс, и если сообщение имеет только его заголовок, загружаются в OST, можно запустить синхронизацию, который пытается загрузить сообщение целиком. 
  
Если вы используете `IID_IMessageRaw` или `IID_IMessage` для запроса интерфейс **IMessage** интерфейсы, которые будут возвращены идентичны используется. Интерфейс **IMessage** , который был запрошен с помощью `IID_IMessageRaw` возвращает сообщение электронной почты, как он существует в OST и не принудительную синхронизацию. 
  
Приведенный ниже показано, как вызывать метод **OpenEntry** , передав `IID_IMessageRaw` вместо `IID_IMessage`.
  
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

Метод **OpenEntry** возвращает код ошибки **MAPI_E_INTERFACE_NOT_SUPPORTED** , указывает, что хранилище сообщений не поддерживает доступ к сообщение в необработанные данные. В этом случае повторите метод **OpenEntry** , передав `IID_IMessage`.

> [!IMPORTANT]
>  `IID_IMessageRaw`не могут быть определены в файле загружаемых заголовка, который в настоящий момент. В этом случае можно добавить его в код с помощью следующее определение. Используйте макрос DEFINE_OLEGUID, определенного в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления символическое имя GUID с его значение. >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

