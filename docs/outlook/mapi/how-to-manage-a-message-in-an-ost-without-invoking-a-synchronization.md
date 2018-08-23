---
title: Управление сообщениями в OST без вызова синхронизации в режиме кэширования данных Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3a1f0aa2-813f-222c-f871-0501de5d9dec
description: Содержит пример кода на C++, в котором показано, как использовать IID_IMessageRaw в IMsgStore::OpenEntry для получения IMessage интерфейса, который управляет сообщения в файле автономной папки (OST) без перезагрузки на загрузку сообщений целиком, если клиентом является в кэширования данных Exchange Режим.
ms.openlocfilehash: f094f5a7deae705ed64b912483726aeb409fb107
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568107"
---
# <a name="manage-messages-in-ost-without-invoking-a-synchronization-in-cached-exchange-mode"></a><span data-ttu-id="7f8bd-103">Управление сообщениями в OST без вызова синхронизации в режиме кэширования данных Exchange</span><span class="sxs-lookup"><span data-stu-id="7f8bd-103">Manage messages in OST without invoking a synchronization in Cached Exchange mode</span></span>

<span data-ttu-id="7f8bd-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f8bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f8bd-105">В этом разделе содержится пример кода на C++, в котором показано, как использовать `IID_IMessageRaw` в **[IMsgStore::OpenEntry](imsgstore-openentry.md)** для получения **[IMessage](imessageimapiprop.md)** интерфейса, который управляет сообщения в файле автономной папки (OST) без перезагрузки загрузки всей сообщение клиента работает в режиме кэширования данных Exchange.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-105">This topic contains a code sample in C++ that shows how to use `IID_IMessageRaw` in **[IMsgStore::OpenEntry](imsgstore-openentry.md)** to obtain an **[IMessage](imessageimapiprop.md)** interface that manages a message in an offline folders file (OST) without forcing a download of the whole message when the client is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="7f8bd-106">Если клиент входит в режиме кэширования Exchange, сообщения в OST может быть в одном из двух режимов:</span><span class="sxs-lookup"><span data-stu-id="7f8bd-106">When a client is in Cached Exchange Mode, messages in the OST can be in one of two states:</span></span>
  
- <span data-ttu-id="7f8bd-107">Загрузить целиком сообщения, содержащего заголовок и тело.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-107">The whole message that contains the header and the body is downloaded.</span></span>
    
- <span data-ttu-id="7f8bd-108">Загрузить сообщение с только его заголовок.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-108">The message with only its header is downloaded.</span></span>
    
<span data-ttu-id="7f8bd-109">Когда запросить интерфейс **IMessage** сообщения в автономной папки и клиент — в режиме кэширования Exchange, используйте `IID_IMessageRaw`.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-109">When you request an **IMessage** interface for a message in an OST and the client is in Cached Exchange Mode, use  `IID_IMessageRaw`.</span></span> <span data-ttu-id="7f8bd-110">Если вы используете `IID_IMessage` для запроса **IMessage** интерфейс, и если сообщение имеет только его заголовок, загружаются в OST, можно запустить синхронизацию, который пытается загрузить сообщение целиком.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-110">If you use  `IID_IMessage` to request an **IMessage** interface, and if the message has only its header downloaded in the OST, you invoke a synchronization that attempts to download the whole message.</span></span> 
  
<span data-ttu-id="7f8bd-111">Если вы используете `IID_IMessageRaw` или `IID_IMessage` для запроса интерфейс **IMessage** интерфейсы, которые будут возвращены идентичны используется.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-111">If you use  `IID_IMessageRaw` or  `IID_IMessage` to request an **IMessage** interface, the interfaces that are returned are identical in use.</span></span> <span data-ttu-id="7f8bd-112">Интерфейс **IMessage** , который был запрошен с помощью `IID_IMessageRaw` возвращает сообщение электронной почты, как он существует в OST и не принудительную синхронизацию.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-112">The **IMessage** interface that was requested by using  `IID_IMessageRaw` returns an email message as it exists in the OST, and synchronization is not forced.</span></span> 
  
<span data-ttu-id="7f8bd-113">Приведенный ниже показано, как вызывать метод **OpenEntry** , передав `IID_IMessageRaw` вместо `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-113">The following example shows how to call the **OpenEntry** method, passing  `IID_IMessageRaw` instead of  `IID_IMessage`.</span></span>
  
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

<span data-ttu-id="7f8bd-114">Метод **OpenEntry** возвращает код ошибки **MAPI_E_INTERFACE_NOT_SUPPORTED** , указывает, что хранилище сообщений не поддерживает доступ к сообщение в необработанные данные.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-114">If the **OpenEntry** method returns the **MAPI_E_INTERFACE_NOT_SUPPORTED** error code, it indicates that the message store does not support accessing the message in raw mode.</span></span> <span data-ttu-id="7f8bd-115">В этом случае повторите метод **OpenEntry** , передав `IID_IMessage`.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-115">In this situation, try the **OpenEntry** method again by passing  `IID_IMessage`.</span></span>

> [!IMPORTANT]
>  <span data-ttu-id="7f8bd-116">`IID_IMessageRaw`не могут быть определены в файле загружаемых заголовка, который в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-116">`IID_IMessageRaw` might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="7f8bd-117">В этом случае можно добавить его в код с помощью следующее определение.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-117">In this case, you can add it to your code by using the following definition.</span></span> <span data-ttu-id="7f8bd-118">Используйте макрос DEFINE_OLEGUID, определенного в guiddef.h файл заголовка Microsoft Windows Software Development Kit (SDK) для сопоставления символическое имя GUID с его значение.</span><span class="sxs-lookup"><span data-stu-id="7f8bd-118">Use the DEFINE_OLEGUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the GUID symbolic name with its value.</span></span> >  `#if !defined(INITGUID) || defined(USES_IID_IMessageRaw)`>  `DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0);`>  `#endif`
  
## <a name="see-also"></a><span data-ttu-id="7f8bd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7f8bd-119">See also</span></span>

- [<span data-ttu-id="7f8bd-120">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="7f8bd-120">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="7f8bd-121">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="7f8bd-121">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="7f8bd-122">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="7f8bd-122">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)

