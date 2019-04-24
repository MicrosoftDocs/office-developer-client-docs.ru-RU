---
title: Управление сообщениями в OST без вызова синхронизации в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: 'Содержит пример кода на языке C++, который показывает, как использовать Иид_имессажерав в IMsgStore:: OpenEntry, чтобы получить интерфейс IMessage, который управляет сообщением в файле автономных папок (OST) без принудительного скачивания всего сообщения, когда клиент находится в кэшированной среде Exchange Режимов.'
ms.openlocfilehash: e50637b496ff43daedad2df27d027d8a6d0dc743
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316396"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="c6444-103">Управление сообщениями в OST без вызова синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="c6444-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="c6444-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6444-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6444-105">В этом разделе приведен пример кода на языке C++, который показывает, `IID_IMessageRaw` как использовать в **[IMsgStore:: OpenEntry](imsgstore-openentry.md)** , чтобы получить интерфейс **[iMessage](imessageimapiprop.md)** , который управляет сообщением в файле автономных папок (OST) без принудительного скачивания всего сообщения, когда клиент находится в режиме кэширования Exchange.</span><span class="sxs-lookup"><span data-stu-id="c6444-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="c6444-106">Когда клиент находится в режиме кэширования Exchange, сообщения в OST могут находиться в одном из двух состояний:</span><span class="sxs-lookup"><span data-stu-id="c6444-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="c6444-107">Загружаются все сообщения, содержащие заголовок и текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="c6444-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="c6444-108">Загружается сообщение с только заголовком.</span><span class="sxs-lookup"><span data-stu-id="c6444-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="c6444-109">Когда вы запрашиваете интерфейс **iMessage** для сообщения в OST-файле и клиент находится в режиме кэширования Exchange, `IID_IMessageRaw`используйте.</span><span class="sxs-lookup"><span data-stu-id="c6444-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="c6444-110">Если вы `IID_IMessage` запрашиваете интерфейс **iMessage** , и если сообщение содержит только заголовок, загруженный в OST, вы вызываете синхронизацию, которая пытается скачать все сообщение.</span><span class="sxs-lookup"><span data-stu-id="c6444-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="c6444-111">Если вы используете `IID_IMessageRaw` или `IID_IMessage` запрашиваете интерфейс **iMessage** , возвращаемые интерфейсы идентичны.</span><span class="sxs-lookup"><span data-stu-id="c6444-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="c6444-112">Интерфейс **iMessage** , который был запрошен с помощью `IID_IMessageRaw` метода, возвращает сообщение электронной почты в том виде, в котором оно существует в OST, и синхронизация не выполняется принудительно.</span><span class="sxs-lookup"><span data-stu-id="c6444-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="c6444-113">В приведенном ниже примере показано, как вызвать метод **OpenEntry** , `IID_IMessageRaw` передав вместо `IID_IMessage`него.</span><span class="sxs-lookup"><span data-stu-id="c6444-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="c6444-114">Если метод **OpenEntry** возвращает код ошибки **мапи_е_интерфаце_нот_суппортед** , он указывает на то, что хранилище сообщений не поддерживает доступ к сообщению в режиме RAW.</span><span class="sxs-lookup"><span data-stu-id="c6444-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="c6444-115">В этом случае повторите метод **OpenEntry** , передав `IID_IMessage`значение.</span><span class="sxs-lookup"><span data-stu-id="c6444-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="c6444-116">`IID_IMessageRaw`не может быть определен в файле заголовков, которые есть у вас в данный момент.</span><span class="sxs-lookup"><span data-stu-id="c6444-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="c6444-117">В этом случае можно добавить его в код с помощью следующего определения.</span><span class="sxs-lookup"><span data-stu-id="c6444-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="c6444-118">Используйте макрос ДЕФИНЕ_ОЛЕГУИД, определенный в файле заголовка пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) guiddef. h, чтобы связать символьное имя GUID со значением.</span><span class="sxs-lookup"><span data-stu-id="c6444-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="c6444-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c6444-119">See also</span></span>

- [<span data-ttu-id="c6444-120">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="c6444-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="c6444-121">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="c6444-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="c6444-122">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="c6444-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

