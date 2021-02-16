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
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="56923-103">Написание просмотра иерархии</span><span class="sxs-lookup"><span data-stu-id="56923-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="56923-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56923-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56923-105">Просмотр иерархии — это компонент пользовательского интерфейса, используемый для отображения таблиц иерархии контейнеров папок и адресных книг.</span><span class="sxs-lookup"><span data-stu-id="56923-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="56923-106">Читатели иерархии могут отображать члены иерархии на разных уровнях, расширяя и совмесив каждый уровень по требованию.</span><span class="sxs-lookup"><span data-stu-id="56923-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="56923-107">Свойство контейнера, **PR_DEPTH** ([PidTagDepth),](pidtagdepth-canonical-property.md)управляет уровнем, на котором отображается элемент иерархии.</span><span class="sxs-lookup"><span data-stu-id="56923-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="56923-108">Для записей, которые представляют контейнеры или папки адресной книги верхнего **уровня,** PR_DEPTH нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="56923-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="56923-109">Значение этого свойства последовательно добавим для записей на последовательном уровне.</span><span class="sxs-lookup"><span data-stu-id="56923-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="56923-110">То есть, когда пользователь выбирает контейнер верхнего уровня для расширения, отображаются все контейнеры с PR_DEPTH 1. </span><span class="sxs-lookup"><span data-stu-id="56923-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="56923-111">Когда пользователь расширяет один из этих подсайтов,  отображает контейнеры с PR_DEPTH 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="56923-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="56923-112">Читатели иерархии поддерживают различные диапазоны глубин.</span><span class="sxs-lookup"><span data-stu-id="56923-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="56923-113">Для просмотра можно ограничиться одним или двумя уровнями или поддерживать несколько уровней, если в качестве приоритета вы можете отобразить широкие иерархии.</span><span class="sxs-lookup"><span data-stu-id="56923-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="56923-114">Адресная книга предоставляет представление иерархии для контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="56923-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="56923-115">**Доступ к таблице иерархии адресной книги**</span><span class="sxs-lookup"><span data-stu-id="56923-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="56923-116">Вызовите [IAddrBook::OpenEntry, передав](iaddrbook-openentry.md)идентификатор записи null, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="56923-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="56923-117">Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневого контейнера, чтобы получить доступ к таблице иерархии адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="56923-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="56923-118">**Доступ к таблице иерархии хранения сообщений по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="56923-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="56923-119">Вызов [IMAPISession::GetMsgStoresTable для](imapisession-getmsgstorestable.md) доступа к таблице хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="56923-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="56923-120">Создайте ограничение, используя структуру [SPropertyRestriction,](spropertyrestriction.md) чтобы ограничить таблицу только теми **строками,** свойство PR_DEFAULT_STORE [(PidTagDefaultStore)](pidtagdefaultstore-canonical-property.md)имеет свойство TRUE.</span><span class="sxs-lookup"><span data-stu-id="56923-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="56923-121">Вызовите [IMAPITable::FindRow,](imapitable-findrow.md)передав ему **SPropertyRestriction,** чтобы найти строку, представляющую хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56923-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="56923-122">Вызовите [IMAPISession::OpenEntry](imapisession-openentry.md), передав свойство **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)из строки по умолчанию в хранилище сообщений в таблице хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="56923-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="56923-123">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений, чтобы получить **свойство PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId).](pidtagipmsubtreeentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="56923-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="56923-124">Вызовите метод [IMsgStore::OpenEntry](imsgstore-openentry.md) из магазина сообщений, передав свойство **PR_IPM_SUBTREE_ENTRYID,** чтобы открыть корневую папку поддерево IPM в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="56923-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="56923-125">Вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневой папки IPM, чтобы получить доступ к таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="56923-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

