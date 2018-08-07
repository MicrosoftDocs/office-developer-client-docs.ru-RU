---
title: Написание средства просмотра иерархии
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0286696707d268867a5536ef345d0af7909918dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812618"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="b0fe7-103">Написание средства просмотра иерархии</span><span class="sxs-lookup"><span data-stu-id="b0fe7-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="b0fe7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0fe7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0fe7-105">Просмотр иерархии — компонент пользовательского интерфейса, который используется для отображения папки и адресной книги контейнер таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="b0fe7-106">Средства просмотра иерархии может отображать элементы иерархии на разных уровнях, развертывание и контракт каждого уровня по запросу.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="b0fe7-107">Свойство контейнера, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) определяет уровень отображения элемент иерархии.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="b0fe7-108">Элементы, соответствующие контейнеры верхнего уровня адресной книги или папки, имеют свойство **PR_DEPTH** равным нулю.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="b0fe7-109">Значение этого свойства последовательно увеличивается для записи в последовательный уровни.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="b0fe7-110">То есть когда пользователь выбирает верхнего уровня контейнер, чтобы развернуть, отображение всех контейнеров с **PR_DEPTH** значение 1.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="b0fe7-111">Когда пользователь раскрывает один из этих субконтейнеров, отображение контейнеров с набором **PR_DEPTH** 2 и так далее.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="b0fe7-112">Средства просмотра иерархии поддерживают различные диапазон глубины.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="b0fe7-113">Можно ограничить используемого средства просмотра для уровней только один или два или если отображение обширный иерархии приоритет может поддерживать несколько уровней.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="b0fe7-114">В адресной книге предоставляет средство просмотра иерархии для контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="b0fe7-115">**Для доступа к таблице иерархии адресной книги**</span><span class="sxs-lookup"><span data-stu-id="b0fe7-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="b0fe7-116">Вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md), передав идентификатор значение null, запись, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="b0fe7-117">Вызов метода [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) корневой контейнер для доступа к таблице иерархии адресной книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="b0fe7-118">**Для доступа к таблице иерархии хранилища сообщений по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="b0fe7-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="b0fe7-119">Вызов [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) для доступа к таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="b0fe7-120">Выполните построение ограничение с помощью структуры [SPropertyRestriction](spropertyrestriction.md) для ограничения в таблице, чтобы только строки, **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) свойство должно быть указано значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="b0fe7-121">Вызовите [IMAPITable::FindRow](imapitable-findrow.md), передав ее **SPropertyRestriction**, чтобы найти строки, представляющие хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="b0fe7-122">Вызовите [IMAPISession::OpenEntry](imapisession-openentry.md), передав в свойстве **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из хранилища сообщений по умолчанию строку в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="b0fe7-123">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0fe7-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="b0fe7-124">Вызовите метод [IMsgStore::OpenEntry](imsgstore-openentry.md) хранилища сообщений, передав свойство **PR_IPM_SUBTREE_ENTRYID** , чтобы открыть корневую папку поддерева IPM хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="b0fe7-125">Вызов метода [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) IPM корневую папку для доступа к его таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="b0fe7-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

