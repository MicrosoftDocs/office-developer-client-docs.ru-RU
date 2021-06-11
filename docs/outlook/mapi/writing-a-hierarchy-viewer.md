---
title: Написание просмотра иерархии
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421132"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="e1a1d-103">Написание просмотра иерархии</span><span class="sxs-lookup"><span data-stu-id="e1a1d-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="e1a1d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1a1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1a1d-105">Зритель иерархии — это компонент пользовательского интерфейса, используемый для отображения таблиц иерархии контейнеров папок и адресных книг.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="e1a1d-106">Зрители иерархии могут отображать членов иерархии на разных уровнях, расширяя и заключая контракты на каждом уровне по запросу.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="e1a1d-107">Свойство контейнера **PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)контролирует уровень отображения члена иерархии.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="e1a1d-108">Записи, которые представляют контейнеры или папки с адресной книгой **верхнего уровня,** имеют свойство PR_DEPTH к нулю.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="e1a1d-109">Значение этого свойства последовательно приумножено для записей на последовательном уровне.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="e1a1d-110">То есть, когда пользователь выбирает для расширения контейнер верхнего уровня, отобразить все контейнеры с PR_DEPTH 1. </span><span class="sxs-lookup"><span data-stu-id="e1a1d-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="e1a1d-111">Когда пользователь расширяет один из этих субконтейнов,  отобразить контейнеры с PR_DEPTH 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="e1a1d-112">Зрители иерархии поддерживают различные диапазоны глубин.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="e1a1d-113">Можно ограничить просмотр только одним или двумя уровнями или поддерживать несколько уровней, если приоритет отобразить экспансивную иерархию.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="e1a1d-114">Адресная книга предоставляет зрителю иерархию для контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="e1a1d-115">**Доступ к таблице иерархии адресных книг**</span><span class="sxs-lookup"><span data-stu-id="e1a1d-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="e1a1d-116">Вызов [IAddrBook::OpenEntry,](iaddrbook-openentry.md)передав идентификатор записи null, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="e1a1d-117">Вызов метода [IMAPIContainer корневого контейнера::GetHierarchyTable,](imapicontainer-gethierarchytable.md) чтобы получить доступ к таблице иерархии адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="e1a1d-118">**Доступ к таблице иерархии магазина сообщений по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="e1a1d-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="e1a1d-119">Вызов [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) чтобы получить доступ к таблице хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="e1a1d-120">Создайте ограничение с помощью [структуры SPropertyRestriction,](spropertyrestriction.md) чтобы ограничить таблицу только теми строками, которые имеют **свойство PR_DEFAULT_STORE** [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)для true.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="e1a1d-121">Вызов [IMAPITable::FindRow](imapitable-findrow.md), передав его **SPropertyRestriction**, чтобы найти строку, представляющую хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="e1a1d-122">Вызов [IMAPISession::OpenEntry](imapisession-openentry.md), передача свойства **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)из строки магазина сообщений по умолчанию в таблице хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="e1a1d-123">Для получения свойства[PR_IPM_SUBTREE_ENTRYID (PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)вызываем метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений. </span><span class="sxs-lookup"><span data-stu-id="e1a1d-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="e1a1d-124">Вызов метода [IMsgStore::OpenEntry](imsgstore-openentry.md) магазина сообщений, **передав** свойство PR_IPM_SUBTREE_ENTRYID, чтобы открыть корневую папку подтриба IPM магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="e1a1d-125">Вызов метода IPM корневой папки [IMAPIContainer::GetHierarchyTable,](imapicontainer-gethierarchytable.md) чтобы получить доступ к таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="e1a1d-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

