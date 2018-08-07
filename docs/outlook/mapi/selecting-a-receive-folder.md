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
ms.openlocfilehash: 87f8b4f4011e405d9848f12b5cae56f27fff1ab8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812222"
---
# <a name="selecting-a-receive-folder"></a><span data-ttu-id="a39bb-103">Выбор папки получения</span><span class="sxs-lookup"><span data-stu-id="a39bb-103">Selecting a Receive Folder</span></span>

  
  
<span data-ttu-id="a39bb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a39bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a39bb-105">Получение папки — там, где размещены входящие сообщения определенного класса.</span><span class="sxs-lookup"><span data-stu-id="a39bb-105">A receive folder is where incoming messages of a particular class are placed.</span></span> <span data-ttu-id="a39bb-106">IPM и связанных с ними отчет о сообщениях MAPI назначает папки «Входящие», как получить папку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a39bb-106">For IPM and related report messages, MAPI assigns the Inbox as the default receive folder.</span></span> <span data-ttu-id="a39bb-107">Для производственных Издержек и связанных с ними отчет о сообщениях MAPI назначает корневую папку хранилища сообщений, как получение папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a39bb-107">For IPC and related report messages, MAPI assigns the root folder of the message store as the default receive folder.</span></span> <span data-ttu-id="a39bb-108">Можно изменить эти назначения или внести дополнительные назначения для других классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="a39bb-108">You can change these assignments or make additional assignments for other message classes.</span></span> <span data-ttu-id="a39bb-109">Внесения явные получать папки назначения для вашего клиента поддерживаемых сообщение классы является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a39bb-109">Making explicit receive folder assignments for your client's supported message classes is optional.</span></span>
  
<span data-ttu-id="a39bb-110">Классом входящие сообщения не содержит папку назначенных получения, поставщик хранения сообщений автоматически использует папку получения для класса, которая соответствует дольше возможные префикс входящих класса.</span><span class="sxs-lookup"><span data-stu-id="a39bb-110">When an incoming message class does not have an assigned receive folder, the message store provider automatically uses the receive folder for the class that matches the longest possible prefix of the incoming class.</span></span> <span data-ttu-id="a39bb-111">Например, если клиент получает сообщение класса IPM. Получать Note.MyDocument и только в папке, где было установлено папки "Входящие" IPM сообщений, а это сообщение будет помещен в папке "Входящие", так как IPM. Note.MyDocument является производным от базового класса IPM.</span><span class="sxs-lookup"><span data-stu-id="a39bb-111">For example, if your client receives a message of class IPM.Note.MyDocument and the only receive folder that has been established is the Inbox for IPM messages, this message will be placed in the Inbox because IPM.Note.MyDocument derives from the base class IPM.</span></span>
  
<span data-ttu-id="a39bb-112">При назначении папки приема сообщений производственных Издержек, никогда не использовать папку из поддерева IPM.</span><span class="sxs-lookup"><span data-stu-id="a39bb-112">When you are assigning a receive folder for IPC messages, never use a folder from the IPM subtree.</span></span> <span data-ttu-id="a39bb-113">Эти папки необходимо зарезервировать IPM только для сообщений.</span><span class="sxs-lookup"><span data-stu-id="a39bb-113">These folders should be reserved for IPM messages only.</span></span> <span data-ttu-id="a39bb-114">Вместо этого используйте в папку, которая находится в пределах корневой папки хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a39bb-114">Use instead a folder that is contained within the message store's root folder.</span></span> 
  
 <span data-ttu-id="a39bb-115">**Чтобы создать папку получения для класса сообщений IPM**</span><span class="sxs-lookup"><span data-stu-id="a39bb-115">**To create a receive folder for an IPM message class**</span></span>
  
1. <span data-ttu-id="a39bb-116">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a39bb-116">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="a39bb-117">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с **PR_IPM_SUBTREE_ENTRYID** как идентификатор записи для открытия в корневую папку поддерева IPM в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a39bb-117">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with **PR_IPM_SUBTREE_ENTRYID** as the entry identifier to open the root folder of the IPM subtree in the message store.</span></span> 
    
3. <span data-ttu-id="a39bb-118">Вызовите [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) , чтобы создать папку получения.</span><span class="sxs-lookup"><span data-stu-id="a39bb-118">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
4. <span data-ttu-id="a39bb-119">Вызов [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) для сопоставления на новую папку в класс сообщения IPM.</span><span class="sxs-lookup"><span data-stu-id="a39bb-119">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPM message class.</span></span> 
    
 <span data-ttu-id="a39bb-120">**Чтобы создать папку получения для классом сообщения производственных Издержек**</span><span class="sxs-lookup"><span data-stu-id="a39bb-120">**To create a receive folder for an IPC message class**</span></span>
  
1. <span data-ttu-id="a39bb-121">Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором запись значение null, чтобы открыть корневую папку хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="a39bb-121">Call [IMsgStore::OpenEntry](imsgstore-openentry.md) with a null entry identifier to open the root folder of the message store.</span></span> 
    
2. <span data-ttu-id="a39bb-122">Вызовите [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) , чтобы создать папку получения.</span><span class="sxs-lookup"><span data-stu-id="a39bb-122">Call [IMAPIFolder::CreateFolder](imapifolder-createfolder.md) to create the receive folder.</span></span> 
    
3. <span data-ttu-id="a39bb-123">Вызов [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) для сопоставления на новую папку в класс сообщения производственных Издержек.</span><span class="sxs-lookup"><span data-stu-id="a39bb-123">Call [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) to map the new folder to your IPC message class.</span></span> 
    
<span data-ttu-id="a39bb-124">Назначьте папку получения, которая используется для сообщений, для сообщений, связанных с ними отчета.</span><span class="sxs-lookup"><span data-stu-id="a39bb-124">Assign the receive folder that you use for messages for related report messages.</span></span> <span data-ttu-id="a39bb-125">Например, если клиент получает IPM. Примечание сообщения, настроить один получать папку для будущего IPM. Примечание сообщения и то же получать папку для последующих сообщений Report.IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="a39bb-125">For example, if your client receives IPM.Note messages, set up one receive folder for future IPM.Note messages and the same receive folder for future Report.IPM.Note messages.</span></span>
  

