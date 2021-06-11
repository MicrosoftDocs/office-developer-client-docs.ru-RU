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
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="cb5f0-103">Управление сообщениями в OST без ссылки на синхронизацию в режиме кэширования Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="cb5f0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cb5f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cb5f0-105">В этом разделе содержится пример кода в C++, который показывает, как использовать `IID_IMessageRaw` **[в IMsgStore::OpenEntry](imsgstore-openentry.md)** для получения интерфейса **[IMessage,](imessageimapiprop.md)** который управляет сообщением в файле автономных папок (OST), не принуждая скачивать все сообщение, когда клиент находится в кэшировать Exchange Mode.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="cb5f0-106">Когда клиент находится в режиме кэш Exchange, сообщения в OST могут быть в одном из двух штатов:</span><span class="sxs-lookup"><span data-stu-id="cb5f0-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="cb5f0-107">Скачано все сообщение, содержаное заголовка и тело.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="cb5f0-108">Скачивается сообщение с только загонами.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="cb5f0-109">При запросе **интерфейса IMessage** для сообщения в OST и клиент находится в режиме кэш Exchange, используйте `IID_IMessageRaw` .</span><span class="sxs-lookup"><span data-stu-id="cb5f0-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="cb5f0-110">Если вы используете для запроса  `IID_IMessage` **интерфейса IMessage** и если в сообщении есть только его загон, загруженный в OST, вы вызываете синхронизацию, которая пытается скачать все сообщение.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="cb5f0-111">При использовании  `IID_IMessageRaw` или  `IID_IMessage` запросе **интерфейса IMessage** возвращенные интерфейсы идентичны по использованию.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="cb5f0-112">Интерфейс **IMessage,** который был запрошен с помощью возвращает сообщение электронной почты, так как оно существует в OST, и синхронизация  `IID_IMessageRaw` не является принудительной.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="cb5f0-113">В следующем примере показано, как вызвать метод **OpenEntry,** передав  `IID_IMessageRaw` вместо  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="cb5f0-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="cb5f0-114">Если метод **OpenEntry** возвращает  код ошибки MAPI_E_INTERFACE_NOT_SUPPORTED, он указывает, что хранилище сообщений не поддерживает доступ к сообщению в сыром режиме.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="cb5f0-115">В этой ситуации попробуйте метод **OpenEntry** еще раз, передав  `IID_IMessage` .</span><span class="sxs-lookup"><span data-stu-id="cb5f0-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="cb5f0-116">`IID_IMessageRaw` может быть не определено в загружаемом файле загона, который у вас есть в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="cb5f0-117">В этом случае вы можете добавить его в код с помощью следующего определения.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="cb5f0-118">Используйте макрос DEFINE_OLEGUID, определенный в файле guiddef.h Windows набора разработки программного обеспечения (SDK), чтобы связать символическое имя GUID с его значением.</span><span class="sxs-lookup"><span data-stu-id="cb5f0-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="cb5f0-119">См. также</span><span class="sxs-lookup"><span data-stu-id="cb5f0-119">See also</span></span>

- [<span data-ttu-id="cb5f0-120">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="cb5f0-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="cb5f0-121">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="cb5f0-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="cb5f0-122">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="cb5f0-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

