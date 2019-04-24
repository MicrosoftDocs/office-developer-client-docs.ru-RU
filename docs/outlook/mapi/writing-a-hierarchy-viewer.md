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
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325643"
---
# <a name="writing-a-hierarchy-viewer"></a><span data-ttu-id="d6ac5-103">Написание средства просмотра иерархии</span><span class="sxs-lookup"><span data-stu-id="d6ac5-103">Writing a Hierarchy Viewer</span></span>

  
  
<span data-ttu-id="d6ac5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6ac5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6ac5-105">Средство просмотра иерархии — это компонент пользовательского интерфейса, используемый для отображения таблиц иерархии контейнеров папок и адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-105">A hierarchy viewer is a user interface component that is used for displaying folder and address book container hierarchy tables.</span></span> <span data-ttu-id="d6ac5-106">Пользователи, просматривающие иерархию, могут отображать элементы иерархии на разных уровнях, расширяя и променяя каждый уровень по запросу.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-106">Hierarchy viewers can display members of the hierarchy at different levels, expanding and contracting each level on demand.</span></span>
  
<span data-ttu-id="d6ac5-107">Свойство Container, **пр_депс** ([PidTagDepth](pidtagdepth-canonical-property.md)), управляет уровнем, на котором отображается элемент иерархии.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-107">The container property, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controls the level at which a hierarchy member is displayed.</span></span> <span data-ttu-id="d6ac5-108">Для записей, представляющих контейнеры и папки адресной книги верхнего уровня, свойству **пр_депс** присвоено нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-108">Entries that represent top-level address book containers or folders have their **PR_DEPTH** property set to zero.</span></span> <span data-ttu-id="d6ac5-109">Значение этого свойства увеличивается последовательно для записей последовательного уровня.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-109">The value of this property is incremented sequentially for entries in sequential levels.</span></span> <span data-ttu-id="d6ac5-110">То есть когда пользователь выбирает контейнер верхнего уровня для расширения, отображает все контейнеры с **пр_депс** , для которых задано значение 1.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-110">That is, when a user selects a top-level container to expand, display all containers with **PR_DEPTH** set to 1.</span></span> <span data-ttu-id="d6ac5-111">Когда пользователь разворачивает один из этих подконтейнеров, отобразите контейнеры с **пр_депс** , равными 2, и т. д.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-111">When a user expands one of these subcontainers, display the containers with **PR_DEPTH** set to 2, and so on.</span></span> 
  
<span data-ttu-id="d6ac5-112">Пользователи, просматривающие иерархию, поддерживают разный диапазон глубины.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-112">Hierarchy viewers support a different range of depths.</span></span> <span data-ttu-id="d6ac5-113">Вы можете ограничить просмотр только одним или двумя уровнями или поддерживать несколько уровней, если для отображения обширной иерархии используется приоритет.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-113">You can limit your viewer to only one or two levels or you can support multiple levels, if displaying an expansive hierarchy is a priority.</span></span> 
  
<span data-ttu-id="d6ac5-114">Адресная книга предоставляет средство просмотра иерархий для контейнеров верхнего уровня в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-114">The address book provides a hierarchy viewer for the top-level containers in the address book.</span></span> 
  
 <span data-ttu-id="d6ac5-115">**Доступ к таблице иерархий адресной книги**</span><span class="sxs-lookup"><span data-stu-id="d6ac5-115">**To access the address book hierarchy table**</span></span>
  
1. <span data-ttu-id="d6ac5-116">Call [IAddrBook:: OpenEntry](iaddrbook-openentry.md), передавая идентификатор записи null, чтобы открыть корневой контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-116">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing a null entry identifier, to open the address book's root container.</span></span>
    
2. <span data-ttu-id="d6ac5-117">ВыЗовите метод [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md) корневого контейнера для доступа к таблице иерархий АДРЕСНОЙ книги MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-117">Call the root container's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access the hierarchy table of the MAPI address book.</span></span> 
    
 <span data-ttu-id="d6ac5-118">**Доступ к таблице иерархии хранилища сообщений по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="d6ac5-118">**To access the default message store's hierarchy table**</span></span>
  
1. <span data-ttu-id="d6ac5-119">Call [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) для доступа к таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-119">Call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to access the message store table.</span></span> 
    
2. <span data-ttu-id="d6ac5-120">Создайте ограничение с помощью структуры [спропертирестриктион](spropertyrestriction.md) , чтобы ограничить таблицу только теми строками, у которых для свойства **пр_дефаулт_сторе** ([PIDTAGDEFAULTSTORE](pidtagdefaultstore-canonical-property.md)) задано значение true.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-120">Build a restriction using the [SPropertyRestriction](spropertyrestriction.md) structure to limit the table to only those rows that have a **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property set to TRUE.</span></span> 
    
3. <span data-ttu-id="d6ac5-121">Вызов [IMAPITable:: FindRow](imapitable-findrow.md), передавая его **спропертирестриктион**, чтобы определить, где находится строка, представляющая хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-121">Call [IMAPITable::FindRow](imapitable-findrow.md), passing it the **SPropertyRestriction**, to locate the row representing the default message store.</span></span> 
    
4. <span data-ttu-id="d6ac5-122">Call [IMAPISession:: OpenEntry](imapisession-openentry.md), передавая свойство **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) из строки хранилища сообщений по умолчанию в таблице хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-122">Call [IMAPISession::OpenEntry](imapisession-openentry.md), passing in the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property from the default message store's row in the message store table.</span></span>
    
5. <span data-ttu-id="d6ac5-123">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) -PROPS хранилища сообщений для получения свойства **пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d6ac5-123">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property.</span></span>
    
6. <span data-ttu-id="d6ac5-124">ВыЗовите метод [IMsgStore:: OpenEntry](imsgstore-openentry.md) хранилища сообщений, передав свойство **пр_ипм_субтри_ентрид** , чтобы открыть корневую папку поддерева IPM хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-124">Call the message store's [IMsgStore::OpenEntry](imsgstore-openentry.md) method, passing the **PR_IPM_SUBTREE_ENTRYID** property, to open the root folder of the message store's IPM subtree.</span></span> 
    
7. <span data-ttu-id="d6ac5-125">ВыЗовите метод [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md) корневой папки IPM, чтобы получить доступ к своей таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="d6ac5-125">Call the IPM root folder's [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method to access its hierarchy table.</span></span> 
    

