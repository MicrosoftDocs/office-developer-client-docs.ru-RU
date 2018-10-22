---
title: Отображение папок в хранилищах сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 62f50ed7925305eca7432da17130d2be0365ef03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582597"
---
# <a name="exposing-folders-in-message-stores"></a><span data-ttu-id="33b77-103">Отображение папок в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="33b77-103">Exposing Folders in Message Stores</span></span>

  
  
<span data-ttu-id="33b77-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="33b77-p101">Каждый поставщик услуг хранилища должен предоставить интерфейс [IMAPIFolder](imapifolderimapicontainer.md) верхнего уровня для клиентских приложений. Папка верхнего уровня соответствует всему хранилищу сообщений; она обеспечивает доступ к папкам, которые пользователь видит в качестве содержимого хранилища сообщений. Кроме того, папка верхнего уровня часто используется по умолчанию в качестве папки для входящих IPC сообщений, а также в качестве папки, из которой отправляются отчеты о прочтении письма. Поставщики хранилища сообщений также должны предоставить поддерево IPM — набор папок, используемых для размещения IPM сообщений — для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="33b77-p101">Every message store provider must present a top-level [IMAPIFolder](imapifolderimapicontainer.md) interface to client applications. The top-level folder corresponds to the entire message store; it provides access to the folders that users see as the contents of the message store. In addition, the top-level folder is often used as the default receive folder for IPC messages and as the folder from which read reports are sent. Message store providers must also present an IPM subtree — a set of folders used to contain IPM messages — to client applications.</span></span> 
  
<span data-ttu-id="33b77-p102">Клиентские приложения могут открывать папку верхнего уровня, вызвав метод[IMsgStore::OpenEntry](imsgstore-openentry.md) со значением 0 и NULL для параметров_cbEntryId_ и _lpEntryId_ соответственно. Тем не менее, в большинстве случаев, клиентские приложения открывают набор папок, который содержит IPM сообщения.</span><span class="sxs-lookup"><span data-stu-id="33b77-p102">Client applications can open the top-level folder by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with 0 and NULL for the  _cbEntryId_ and  _lpEntryId_ parameters, respectively. In most cases, however, client applications open the set of folders that contain IPM messages.</span></span> 
  
<span data-ttu-id="33b77-111">Для получения списка папок в дереве папок IPM хранилища сообщений, выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="33b77-111">To get a list of folders in the message store's IPM folder tree, use the following procedure:</span></span>
  
1. <span data-ttu-id="33b77-112">С помощью сессии выполните вызов метода MAPI [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="33b77-112">Use your MAPI session to call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method.</span></span> 
    
2. <span data-ttu-id="33b77-113">Используйте указатель полученной базы данных сообщений для вызова метода [IMAPIProp::GetProps](imapiprop-getprops.md) для свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="33b77-113">Use the resulting message database pointer to call the [IMAPIProp::GetProps](imapiprop-getprops.md) method for the **PR_IPM_SUBTREE_ENTRYID** ( [PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
3. <span data-ttu-id="33b77-114">Вызовите метод[IMsgStore::OpenEntry](imsgstore-openentry.md) с идентификатором записи, чтобы получить указатель **IMAPIFolder**.</span><span class="sxs-lookup"><span data-stu-id="33b77-114">Call the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with the entry identifier to get an **IMAPIFolder** pointer.</span></span> 
    
4. <span data-ttu-id="33b77-115">Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) для получения таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="33b77-115">Call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to get a table of the contents of the folder.</span></span> 
    
5. <span data-ttu-id="33b77-116">Вызовите метод [IMAPITable::QueryRows](imapitable-queryrows.md) для получения списка папок в папке верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="33b77-116">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to list the folders in the top-level folder.</span></span> 
    
<span data-ttu-id="33b77-p103">Клиенты MAPI используют эти папки для доступа к прочим объектам папки и объектам сообщений из хранилища сообщений. **IMAPIFolder**и его родительский интерфейс [IMAPIContainer](imapicontainerimapiprop.md), содержат методы, которые ваш поставщик услуг хранилища сообщений должен использовать для заполнения папки объектами сообщения и ответа на запросы клиента для выполнения операций с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="33b77-p103">MAPI clients use these folders to access other folder objects and message objects in the message store. **IMAPIFolder**, and its parent interface [IMAPIContainer](imapicontainerimapiprop.md), contain the methods your message store provider must implement to populate folders with message objects and respond to client requests to operate on messages.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33b77-119">См. также</span><span class="sxs-lookup"><span data-stu-id="33b77-119">See also</span></span>



[<span data-ttu-id="33b77-120">Реализация папок в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="33b77-120">Implementing Folders in Message Stores</span></span>](implementing-folders-in-message-stores.md)

