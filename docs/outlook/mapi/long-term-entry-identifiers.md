---
title: Долгосрочные идентификаторы записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a514275e-40c2-48db-8072-1dfc392a7ac6
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 589420db48edb348a22f34ce72b948f4d8207ae9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809666"
---
# <a name="long-term-entry-identifiers"></a><span data-ttu-id="8ca23-103">Долгосрочные идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="8ca23-103">Long-Term Entry Identifiers</span></span>

  
  
<span data-ttu-id="8ca23-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ca23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ca23-105">Долгосрочные идентификатор записи назначается поставщиком услуг на объект при объекта требуется идентификатор с длительного времени существования.</span><span class="sxs-lookup"><span data-stu-id="8ca23-105">A long-term entry identifier is assigned by a service provider to an object when an object requires an identifier with a prolonged lifespan.</span></span> <span data-ttu-id="8ca23-106">Долгосрочные идентификаторы записей всегда являются допустимыми для недель или месяцев и могут стать недействительными на других рабочих станций, в зависимости от поставщика.</span><span class="sxs-lookup"><span data-stu-id="8ca23-106">Long-term entry identifiers are always valid for weeks or months and can be valid on other workstations, depending on the provider.</span></span> <span data-ttu-id="8ca23-107">Долгосрочные идентификаторы, созданные с поставщиками адресной книги для получателей универсального действительны.</span><span class="sxs-lookup"><span data-stu-id="8ca23-107">The long-term identifiers created by address book providers for custom recipients are universally valid.</span></span> 
  
<span data-ttu-id="8ca23-108">Долгосрочные идентификаторы записей назначаются хранилищ сообщений, папок, сообщения, контейнеров адресной книги, обмена мгновенными сообщениями пользователи и рассылки списков.</span><span class="sxs-lookup"><span data-stu-id="8ca23-108">Long-term entry identifiers are assigned to message stores, folders, messages, address book containers, messaging users, and distribution lists.</span></span> <span data-ttu-id="8ca23-109">Клиентские приложения вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) этих объектов, всегда открывается долгосрочного идентификатор записи, который возвращается.</span><span class="sxs-lookup"><span data-stu-id="8ca23-109">When client applications call the [IMAPIProp::GetProps](imapiprop-getprops.md) method of these objects, it is always a long-term entry identifier that is returned.</span></span> 
  
<span data-ttu-id="8ca23-110">Долгосрочные идентификаторы записей должно быть уникальным для всех хранилищ сообщений в текущей конфигурации; Таким образом когда сообщение или папку из одного хранилища копируется в другую, его необходимо назначить новый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="8ca23-110">Long-term entry identifiers must be unique across all message stores in the active profile; therefore, when a message or folder is copied from one message store to another, it must be assigned a new entry identifier.</span></span> <span data-ttu-id="8ca23-111">При перемещении объекта хранилища сообщений поставщика хранилища сообщений, который реализует move определяет, будет ли исходный идентификатор записи остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="8ca23-111">When a message store object is moved, the message store provider that implements the move determines whether the original entry identifier will remain valid.</span></span> <span data-ttu-id="8ca23-112">Некоторые поставщики услуг назначить новые идентификаторы записей перемещенной объектов; некоторые — нет.</span><span class="sxs-lookup"><span data-stu-id="8ca23-112">Some service providers assign new entry identifiers to moved objects; others do not.</span></span> <span data-ttu-id="8ca23-113">При изменении новый идентификатор записи будут включены в сведениях о передается клиентов, когда они будут уведомлены об переход.</span><span class="sxs-lookup"><span data-stu-id="8ca23-113">If there is a change, the new entry identifier will be included in the information passed to clients when they are notified of the move.</span></span> 
  
<span data-ttu-id="8ca23-114">Как правило поставщиков хранилища сообщений реализовать следующее поведение при перемещении папок:</span><span class="sxs-lookup"><span data-stu-id="8ca23-114">Typically, message store providers implement the following behavior when they move folders:</span></span>
  
- <span data-ttu-id="8ca23-115">При перемещении папку из одного хранилища в другом хранилище другого типа, идентификатор записи гарантированно изменить.</span><span class="sxs-lookup"><span data-stu-id="8ca23-115">When a folder is moved from one message store to another store of a different type, the entry identifier is guaranteed to change.</span></span>
    
- <span data-ttu-id="8ca23-116">При перемещении папку из одного хранилища в другом хранилище того же типа, почти всегда изменяется идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="8ca23-116">When a folder is moved from one message store to another store of the same type, the entry identifier almost always changes.</span></span>
    
- <span data-ttu-id="8ca23-117">При перемещении папки в другое место в пределах одного хранилища сообщений, идентификатор записи может или не может изменяться, в зависимости от поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="8ca23-117">When a folder is moved to another location within the same message store, the entry identifier might or might not change, depending on the message store provider.</span></span>
    
<span data-ttu-id="8ca23-118">Переименование папки без изменения родительской папки обычно не вызывает идентификатор записи для изменения.</span><span class="sxs-lookup"><span data-stu-id="8ca23-118">Renaming a folder without changing its parent folder usually does not cause the entry identifier to change.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ca23-119">См. также</span><span class="sxs-lookup"><span data-stu-id="8ca23-119">See also</span></span>



[<span data-ttu-id="8ca23-120">Идентификаторы MAPI записей</span><span class="sxs-lookup"><span data-stu-id="8ca23-120">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

