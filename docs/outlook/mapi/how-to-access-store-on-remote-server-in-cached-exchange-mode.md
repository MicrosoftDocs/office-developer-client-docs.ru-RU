---
title: Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299064"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="dc0d9-103">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="dc0d9-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="dc0d9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc0d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc0d9-105">В этом разделе приведен пример кода на языке C++, в котором показано, как использовать флаг **мапи_но_каче** для открытия папки или сообщения в хранилище сообщений на удаленном сервере, если Microsoft Office Outlook находится в режиме кэширования Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="dc0d9-106">Режим кэширования Exchange позволяет Outlook использовать локальную копию почтового ящика пользователя, в то время как Outlook поддерживает сетевое подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="dc0d9-107">Когда Outlook работает в режиме кэширования Exchange, по умолчанию все решения MAPI, которые выполняют вход в тот же сеанс, также подключаются к кэшированному хранилищу сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="dc0d9-108">Все данные, к которым обращается доступ, и все внесенные изменения вносятся в локальную копию почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="dc0d9-109">Клиент или поставщик услуг может переопределить подключение к локальному хранилищу сообщений и открыть сообщение или папку в удаленном хранилище, установив бит для **мапи_но_каче** в параметре *ulFlags* при вызове **[IMsgStore:: OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="dc0d9-110">В приведенном ниже примере кода показано, как вызывать **IMsgStore:: OpenEntry** с флагом **мапи_но_каче** , установленНым в параметре *ulFlags* , чтобы открыть корневую папку в удаленном хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc0d9-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
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

<span data-ttu-id="dc0d9-111">Если вы открыли хранилище сообщений с флагом **мдб_онлине** на удаленном сервере, не нужно использовать флаг **мапи_но_каче** .</span><span class="sxs-lookup"><span data-stu-id="dc0d9-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dc0d9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="dc0d9-112">See also</span></span>

- [<span data-ttu-id="dc0d9-113">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="dc0d9-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="dc0d9-114">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="dc0d9-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="dc0d9-115">Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="dc0d9-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

