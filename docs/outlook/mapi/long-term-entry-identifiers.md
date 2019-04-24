---
title: Долгосрочные идентификаторы записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b65656992681618aa8a1c53217bdd7101bc2502b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307786"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="2e796-103">Долгосрочные идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="2e796-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="2e796-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e796-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e796-105">Долгосрочный идентификатор записи назначается поставщиком службы объекту, когда объект требует идентификатора с длительным сроком действия.</span><span class="sxs-lookup"><span data-stu-id="2e796-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="2e796-106">Долгосрочные идентификаторы записей всегда действительны для недель и месяцев и могут быть действительными на других рабочих станциях в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="2e796-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="2e796-107">Долгосрочные идентификаторы, созданные поставщиками адресных книг для настраиваемых получателей, являются универсально действительными.</span><span class="sxs-lookup"><span data-stu-id="2e796-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="2e796-108">Долгосрочные идентификаторы записей назначаются хранилищам сообщений, папкам, сообщениям, контейнерам адресных книг, пользователям обмена сообщениями и спискам рассылки.</span><span class="sxs-lookup"><span data-stu-id="2e796-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="2e796-109">Когда клиентские приложения вызывают метод [IMAPIProp::](imapiprop-getprops.md) -PROPS этих объектов, он всегда возвращается в долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="2e796-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="2e796-110">Долгосрочные идентификаторы записей должны быть уникальными для всех хранилищ сообщений в активном профиле; Таким образом, при копировании сообщения или папки из одного хранилища сообщений в другое ему должен быть назначен новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="2e796-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="2e796-111">При перемещении объекта хранилища сообщений поставщик хранилища сообщений, который реализует перемещение, определяет, остается ли действительным исходный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="2e796-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="2e796-112">Некоторые поставщики услуг назначают новые идентификаторы записей перемещенным объектам. другие пользователи не могут.</span><span class="sxs-lookup"><span data-stu-id="2e796-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="2e796-113">При наличии изменений новый идентификатор записи будет включен в данные, передаваемые клиентам при получении им уведомления о перемещении.</span><span class="sxs-lookup"><span data-stu-id="2e796-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="2e796-114">Как правило, поставщики хранилищ сообщений реализуют следующее поведение при перемещении папок:</span><span class="sxs-lookup"><span data-stu-id="2e796-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="2e796-115">Когда папка перемещается из одного хранилища сообщений в другое, идентификатор записи гарантированно изменяется.</span><span class="sxs-lookup"><span data-stu-id="2e796-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="2e796-116">Когда папка перемещается из одного хранилища сообщений в другое, идентификатор записи почти всегда изменяется.</span><span class="sxs-lookup"><span data-stu-id="2e796-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="2e796-117">Когда папка перемещается в другое место в том же хранилище сообщений, идентификатор записи может измениться или может не измениться в зависимости от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e796-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="2e796-118">Переименование папки без изменения ее родительской папки обычно не приводит к изменению идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="2e796-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e796-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2e796-119">See also</span></span>



[<span data-ttu-id="2e796-120">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="2e796-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

