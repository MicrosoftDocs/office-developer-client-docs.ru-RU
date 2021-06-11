---
title: Long-Term идентификаторы входа
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
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="a43e8-103">Long-Term идентификаторы входа</span><span class="sxs-lookup"><span data-stu-id="a43e8-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="a43e8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a43e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a43e8-105">Долгосрочный идентификатор записи назначен поставщиком услуг объекту, если объекту требуется идентификатор с длительным сроком службы.</span><span class="sxs-lookup"><span data-stu-id="a43e8-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="a43e8-106">Идентификаторы долгосрочных записей всегда действительны в течение нескольких недель или месяцев и могут быть действительны на других рабочих станциях в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="a43e8-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="a43e8-107">Долгосрочные идентификаторы, созданные поставщиками адресных книг для настраиваемого получателя, являются универсальными.</span><span class="sxs-lookup"><span data-stu-id="a43e8-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="a43e8-108">Для хранения сообщений, папок, сообщений, контейнеров адресных книг, пользователей сообщений и списков рассылки назначены долгосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="a43e8-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="a43e8-109">При вызове клиентских приложений [методом IMAPIProp::GetProps](imapiprop-getprops.md) этих объектов всегда возвращается долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a43e8-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="a43e8-110">Идентификаторы долгосрочных записей должны быть уникальными во всех хранилищах сообщений в активном профиле; Поэтому при копировании сообщения или папки из одного магазина сообщений в другой ему должен быть назначен новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a43e8-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="a43e8-111">При перемещении объекта хранения сообщений поставщик магазина сообщений, реализуя этот шаг, определяет, будет ли действителен исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a43e8-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="a43e8-112">Некоторые поставщики услуг назначают перемещенным объектам новые идентификаторы записей; другие этого не делают.</span><span class="sxs-lookup"><span data-stu-id="a43e8-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="a43e8-113">При изменении новый идентификатор записи будет включен в сведения, переданные клиентам при уведомлении о переходе.</span><span class="sxs-lookup"><span data-stu-id="a43e8-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="a43e8-114">Обычно поставщики магазинов сообщений реализуют следующее поведение при движении папок:</span><span class="sxs-lookup"><span data-stu-id="a43e8-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="a43e8-115">При перемещении папки из одного магазина сообщений в другой магазин другого типа идентификатор записи гарантированно изменится.</span><span class="sxs-lookup"><span data-stu-id="a43e8-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="a43e8-116">При перемещении папки из одного магазина сообщений в другой магазин того же типа идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="a43e8-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="a43e8-117">При перемещении папки в другое расположение в том же хранилище сообщений идентификатор записи может изменяться или не изменяться в зависимости от поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="a43e8-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="a43e8-118">Переименование папки без изменения родительской папки обычно не вызывает изменения идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="a43e8-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a43e8-119">См. также</span><span class="sxs-lookup"><span data-stu-id="a43e8-119">See also</span></span>



[<span data-ttu-id="a43e8-120">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="a43e8-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

