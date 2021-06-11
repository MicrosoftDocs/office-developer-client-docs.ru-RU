---
title: Выбор папки получения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 144c7179-b390-479f-a2aa-324974f04eba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9151b76f74dead5cac771dbdc091bbee03359aec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428419"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="28d66-103">Выбор папки получения</span><span class="sxs-lookup"><span data-stu-id="28d66-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="28d66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28d66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28d66-105">Папка получения — это место, где размещаются входящие сообщения определенного класса.</span><span class="sxs-lookup"><span data-stu-id="28d66-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="28d66-106">Для сообщений IPM и связанных отчетов MAPI назначает папку "Входящие" как папку получения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28d66-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="28d66-107">Для IPC и связанных сообщений отчетов MAPI назначает корневую папку магазина сообщений в качестве папки получения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28d66-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="28d66-108">Вы можете изменить эти назначения или сделать дополнительные назначения для других классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="28d66-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="28d66-109">Выполнение явных назначений папки получения для поддерживаемых классов сообщений клиента является необязательным.</span><span class="sxs-lookup"><span data-stu-id="28d66-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="28d66-110">Если в классе входящих сообщений нет назначенной папки получения, поставщик магазина сообщений автоматически использует папку получения для класса, который соответствует максимально длинной префиксу входящих классов.</span><span class="sxs-lookup"><span data-stu-id="28d66-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="28d66-111">Например, если клиент получает сообщение об IPM класса. Note.MyDocument и единственная созданная папка для получения — это почтовый ящик для сообщений IPM, это сообщение будет помещено в папку "Входящие", так как IPM. Note.MyDocument происходит от IPM базового класса.</span><span class="sxs-lookup"><span data-stu-id="28d66-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="28d66-112">При назначении папки получения для сообщений IPC никогда не используйте папку из подтриба IPM.</span><span class="sxs-lookup"><span data-stu-id="28d66-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="28d66-113">Эти папки должны быть зарезервированы только для сообщений IPM.</span><span class="sxs-lookup"><span data-stu-id="28d66-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="28d66-114">Вместо этого используйте папку, которая содержится в корневой папке магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="28d66-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="28d66-115">**Создание папки получения для класса сообщений IPM**</span><span class="sxs-lookup"><span data-stu-id="28d66-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="28d66-116">Для получения свойства[PR_IPM_SUBTREE_ENTRYID (PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)вызываем метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений. </span><span class="sxs-lookup"><span data-stu-id="28d66-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="28d66-117">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) PR_IPM_SUBTREE_ENTRYID идентификатором входа, чтобы открыть корневую папку подтриба IPM в хранилище сообщений. </span><span class="sxs-lookup"><span data-stu-id="28d66-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="28d66-118">Вызов [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) для создания папки получения.</span><span class="sxs-lookup"><span data-stu-id="28d66-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="28d66-119">Позвоните [в IMsgStore::SetReceiveFolder,](imsgstore-setreceivefolder.md) чтобы соотвести новую папку с классом сообщений IPM.</span><span class="sxs-lookup"><span data-stu-id="28d66-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="28d66-120">**Создание папки получения для класса сообщений IPC**</span><span class="sxs-lookup"><span data-stu-id="28d66-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="28d66-121">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи null, чтобы открыть корневую папку магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="28d66-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="28d66-122">Вызов [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) для создания папки получения.</span><span class="sxs-lookup"><span data-stu-id="28d66-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="28d66-123">Позвоните [в IMsgStore::SetReceiveFolder,](imsgstore-setreceivefolder.md) чтобы соотвести новую папку с классом сообщений IPC.</span><span class="sxs-lookup"><span data-stu-id="28d66-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="28d66-124">Назначьте папку получения, используемую для сообщений для связанных сообщений отчетов.</span><span class="sxs-lookup"><span data-stu-id="28d66-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="28d66-125">Например, если клиент получает IPM. Примечание сообщений, настройка одной папки получения для будущей IPM. Примечание сообщений и та же папка получения для будущих сообщений Report.IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="28d66-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

