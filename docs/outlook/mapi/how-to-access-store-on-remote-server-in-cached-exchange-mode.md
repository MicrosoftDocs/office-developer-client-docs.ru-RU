---
title: Доступ к хранилищу на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 8f1afd31f017b73fa5270d8fbf4c2a1c8fa08880
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808610"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="d92d3-103">Доступ к хранилищу на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange</span><span class="sxs-lookup"><span data-stu-id="d92d3-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="d92d3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d92d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d92d3-105">В этом разделе содержится пример кода на C++, показано, как использовать флаг **MAPI_NO_CACHE** , чтобы открыть папку или сообщение для хранилища сообщений на удаленном сервере, когда Microsoft Office Outlook находится в режиме кэширования данных Exchange.</span><span class="sxs-lookup"><span data-stu-id="d92d3-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="d92d3-106">Режим кэширования данных Exchange позволяет Outlook на использование локальной копии почтового ящика пользователя во время Outlook устанавливает соединение с удаленной копией почтового ящика пользователя на удаленном сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="d92d3-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="d92d3-107">Когда Outlook работает в режиме кэширования данных Exchange по умолчанию всех решений MAPI, выполните вход на том же сеансе также подключены к хранилище кэшированных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d92d3-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="d92d3-108">Все данные, к которому осуществляется и все изменения, внесенные выполняются к локальной копии почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="d92d3-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="d92d3-109">Клиент или служба поставщика можно переопределить подключения к хранилищу локального сообщения и откройте сообщение или папки для удаленного хранилища, установив бит для **MAPI_NO_CACHE** с помощью параметра *ulFlags* при вызове **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="d92d3-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="d92d3-110">В следующем примере кода показано, как вызывать **IMsgStore::OpenEntry** с флагом **MAPI_NO_CACHE** значение с помощью параметра *ulFlags* откройте корневой папки хранилища удаленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="d92d3-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="d92d3-111">При открытии хранилища сообщений с флагом **MDB_ONLINE** на удаленном сервере, не нужно использовать флаг **MAPI_NO_CACHE** .</span><span class="sxs-lookup"><span data-stu-id="d92d3-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d92d3-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d92d3-112">See also</span></span>

- [<span data-ttu-id="d92d3-113">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="d92d3-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="d92d3-114">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="d92d3-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="d92d3-115">Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="d92d3-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

