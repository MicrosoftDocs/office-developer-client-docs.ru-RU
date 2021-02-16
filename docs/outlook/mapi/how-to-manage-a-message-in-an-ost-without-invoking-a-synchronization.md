---
title: Управление сообщениями в OST без синхронизации в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Содержит пример кода на C++, который показывает, как использовать IID_IMessageRaw в IMsgStore::OpenEntry для получения интерфейса IMessage, который управляет сообщением в файле автономных папок (OST) без принудительной загрузки всего сообщения, когда клиент находится в режиме кэшации Exchange.
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418759"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="a66a6-103">Управление сообщениями в OST без синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="a66a6-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="a66a6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a66a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a66a6-105">В этом разделе содержится пример кода на C++, который показывает, как использовать `IID_IMessageRaw` **[iMsgStore::OpenEntry](imsgstore-openentry.md)** для получения **[интерфейса IMessage,](imessageimapiprop.md)** который управляет сообщением в файле автономных папок (OST) без принудительной загрузки всего сообщения, когда клиент находится в режиме кэшации Exchange.</span><span class="sxs-lookup"><span data-stu-id="a66a6-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="a66a6-106">Если клиент находится в режиме кэшации Exchange, сообщения в OST могут быть в одном из двух режимов:</span><span class="sxs-lookup"><span data-stu-id="a66a6-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="a66a6-107">Скачивание всего сообщения с заголовщиком и текстом.</span><span class="sxs-lookup"><span data-stu-id="a66a6-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="a66a6-108">Загружается сообщение только с заголбом.</span><span class="sxs-lookup"><span data-stu-id="a66a6-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="a66a6-109">Когда вы запрашиваете **интерфейс IMessage** для сообщения в OST и клиент находится в режиме кэшации Exchange, используйте  `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="a66a6-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="a66a6-110">Если вы используете для запроса  `IID_IMessage` **интерфейса IMessage** и у сообщения есть только его загон, загруженный в OST, вы вызываете синхронизацию, которая пытается скачать все сообщение.</span><span class="sxs-lookup"><span data-stu-id="a66a6-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="a66a6-111">При использовании  `IID_IMessageRaw` или  `IID_IMessage` запросе **интерфейса IMessage** возвращаемые интерфейсы используются одинаково.</span><span class="sxs-lookup"><span data-stu-id="a66a6-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="a66a6-112">Интерфейс **IMessage,** который был запрошен с помощью, возвращает сообщение электронной почты в том же качестве, что и в OST, и синхронизация не  `IID_IMessageRaw` является принудительной.</span><span class="sxs-lookup"><span data-stu-id="a66a6-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="a66a6-113">В следующем примере показано, как вызвать метод **OpenEntry,** передав  `IID_IMessageRaw` вместо  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="a66a6-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="a66a6-114">Если метод **OpenEntry** возвращает  код ошибки MAPI_E_INTERFACE_NOT_SUPPORTED, это означает, что хранилище сообщений не поддерживает доступ к сообщению в необработанных режимах.</span><span class="sxs-lookup"><span data-stu-id="a66a6-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="a66a6-115">В этой ситуации еще раз попробуйте **метод OpenEntry,** передав  `IID_IMessage` его.</span><span class="sxs-lookup"><span data-stu-id="a66a6-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="a66a6-116">`IID_IMessageRaw` может не быть определено в загружаемом файле загона, который у вас есть в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="a66a6-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="a66a6-117">В этом случае его можно добавить в код с помощью следующего определения.</span><span class="sxs-lookup"><span data-stu-id="a66a6-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="a66a6-118">Используйте макрос DEFINE_OLEGUID, определенный в файле guiddef.h файла загона SDK, чтобы связать символьное имя GUID с его значением.</span><span class="sxs-lookup"><span data-stu-id="a66a6-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="a66a6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a66a6-119">See also</span></span>

- [<span data-ttu-id="a66a6-120">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="a66a6-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="a66a6-121">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="a66a6-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="a66a6-122">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="a66a6-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

