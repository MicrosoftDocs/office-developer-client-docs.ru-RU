---
title: Long-Term записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409225"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="ffa32-103">Long-Term записей</span><span class="sxs-lookup"><span data-stu-id="ffa32-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="ffa32-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ffa32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ffa32-105">Долгосрочный идентификатор записи, присвоенный поставщиком услуг объекту, когда объекту требуется идентификатор с длительным сроком действия.</span><span class="sxs-lookup"><span data-stu-id="ffa32-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="ffa32-106">Долгосрочные идентификаторы записей всегда действительны в течение недель или месяцев и могут быть действительны на других рабочих станциях в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="ffa32-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="ffa32-107">Долгосрочные идентификаторы, созданные поставщиками адресных книг для настраиваемого получателя, являются универсальными.</span><span class="sxs-lookup"><span data-stu-id="ffa32-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="ffa32-108">Долгосрочные идентификаторы записей назначены хранилищам сообщений, папок, сообщений, контейнерам адресных книг, пользователям сообщений и спискам рассылки.</span><span class="sxs-lookup"><span data-stu-id="ffa32-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="ffa32-109">Когда клиентские приложения звонят [методу IMAPIProp::GetProps](imapiprop-getprops.md) этих объектов, всегда возвращается долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="ffa32-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="ffa32-110">Долгосрочные идентификаторы записей должны быть уникальными во всех хранилищах сообщений в активном профиле; Таким образом, когда сообщение или папка копируется из одного хранилище сообщений в другое, ему должен быть назначен новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="ffa32-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="ffa32-111">При перемещении объекта хранения сообщений поставщик, реализующая перемещение, определяет, будет ли исходный идентификатор записи оставаться действительным.</span><span class="sxs-lookup"><span data-stu-id="ffa32-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="ffa32-112">Некоторые поставщики услуг назначают новые идентификаторы записей перемещенным объектам; другие этого не делают.</span><span class="sxs-lookup"><span data-stu-id="ffa32-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="ffa32-113">При изменении новый идентификатор записи будет включен в информацию, передаемую клиентам при уведомлении о переходе.</span><span class="sxs-lookup"><span data-stu-id="ffa32-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="ffa32-114">Как правило, поставщики store сообщений реализуют следующее поведение при перемещения папок:</span><span class="sxs-lookup"><span data-stu-id="ffa32-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="ffa32-115">При перемещении папки из одного хранилище сообщений в другое хранилище другого типа идентификатор записи гарантированно изменится.</span><span class="sxs-lookup"><span data-stu-id="ffa32-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="ffa32-116">При перемещении папки из одного хранилище сообщений в другое хранилище того же типа идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="ffa32-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="ffa32-117">При перемещении папки в другое расположение в том же хранилище сообщений идентификатор записи может изменяться или не изменяться в зависимости от поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="ffa32-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="ffa32-118">Переименование папки без изменения родительской папки обычно не приведет к изменению идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="ffa32-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffa32-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ffa32-119">See also</span></span>



[<span data-ttu-id="ffa32-120">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="ffa32-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

