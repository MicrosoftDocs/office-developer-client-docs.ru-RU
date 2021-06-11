---
title: Доступ к магазину на удаленном сервере, когда Outlook кэшировали Exchange режиме
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: 'Последнее изменение: 02 июля 2012 г.'
ms.openlocfilehash: 0d977507f6aff8aa5fbf437b4b718486a71f67dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420733"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="c4109-103">Доступ к магазину на удаленном сервере, когда Outlook кэшировали Exchange режиме</span><span class="sxs-lookup"><span data-stu-id="c4109-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="c4109-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4109-105">В этом разделе содержится пример кода в C++, который показывает, как использовать флаг **MAPI_NO_CACHE** для открытия папки или сообщения в хранилище сообщений на удаленном сервере, когда Microsoft Office Outlook находится в кэшировать Exchange режиме.</span><span class="sxs-lookup"><span data-stu-id="c4109-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="c4109-106">Кэш Exchange режим позволяет Outlook использовать локализованную копию почтового ящика пользователя, а Outlook поддерживает подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4109-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="c4109-107">Если Outlook в кэшном режиме Exchange, по умолчанию все решения MAPI, войдите в один сеанс, также подключаются к хранилище кэшных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c4109-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="c4109-108">Все полученные данные и внесенные изменения в локальный экземпляр почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c4109-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="c4109-109">Клиент или поставщик услуг может переопрещать подключение к локальному хранилище сообщений и открыть сообщение  или папку в удаленном магазине, задав бит для MAPI_NO_CACHE *параметра ulFlags* при вызове **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="c4109-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="c4109-110">В следующем примере кода показано, как вызвать **IMsgStore::OpenEntry** с флагом MAPI_NO_CACHE в параметре *ulFlags,* чтобы открыть корневую папку в удаленном хранилище сообщений. </span><span class="sxs-lookup"><span data-stu-id="c4109-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
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

<span data-ttu-id="c4109-111">Если вы открыли хранилище сообщений с флагом **MDB_ONLINE** на удаленном сервере, вам не нужно использовать **MAPI_NO_CACHE** флаг.</span><span class="sxs-lookup"><span data-stu-id="c4109-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4109-112">См. также</span><span class="sxs-lookup"><span data-stu-id="c4109-112">See also</span></span>

- [<span data-ttu-id="c4109-113">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="c4109-113">About MAPI Additions</span></span>](about-mapi-additions.md)
- [<span data-ttu-id="c4109-114">Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="c4109-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="c4109-115">Управление сообщением в OST без вызова синхронизации в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="c4109-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

