---
title: Передачей уведомлений адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808545"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="1dcd3-103">Передачей уведомлений адресной книги</span><span class="sxs-lookup"><span data-stu-id="1dcd3-103">Handing address book notification</span></span>
  
<span data-ttu-id="1dcd3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1dcd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1dcd3-105">Уведомления о адресной книги Разрешить клиенту для получения событий, происходящих для любой записи адресной книги или записи.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="1dcd3-106">Для этих уведомлений через адресной книги MAPI, вызвав [IAddrBook::Advise](iaddrbook-advise.md) или с помощью иерархии контейнер адресной книги или таблицу содержимого можно регистрировать путем вызова [IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="1dcd3-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="1dcd3-107">Укажите идентификатор записи контейнер адресной книги, список рассылки или обмена мгновенными сообщениями пользователя при регистрации уведомлений на конкретной записи и NULL при регистрации уведомлений на всей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="1dcd3-108">Идентификатор записи должен представлять обмена сообщениями пользователя или список рассылки в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="1dcd3-109">**IAddrBook::Advise** проверяет этот идентификатор записи, чтобы определить, какие адресной книги поставщика несет ответственность за соответствующего объекта и перенаправляет вызов метода [IABLogon::Advise](iablogon-advise.md) поставщик соответствующие адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="1dcd3-110">Клиенты могут зарегистрировать для следующих типов событий в адресной книги:</span><span class="sxs-lookup"><span data-stu-id="1dcd3-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="1dcd3-111">Критическая ошибка</span><span class="sxs-lookup"><span data-stu-id="1dcd3-111">Critical error</span></span>
    
- <span data-ttu-id="1dcd3-112">Какие-либо события объекта (создан, изменения, удаления, перемещения или копирования)</span><span class="sxs-lookup"><span data-stu-id="1dcd3-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="1dcd3-113">Изменения в таблице</span><span class="sxs-lookup"><span data-stu-id="1dcd3-113">Table modified</span></span>
    
<span data-ttu-id="1dcd3-114">Как правило Регистрация происходит только для содержимого контейнера адресной книги и таблиц иерархии.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="1dcd3-115">Очень редко, что клиенты регистрируются с низким уровнем системы обмена сообщениями объекты списка пользователей и распространения.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="1dcd3-116">Это, так как:</span><span class="sxs-lookup"><span data-stu-id="1dcd3-116">This is because:</span></span>
  
- <span data-ttu-id="1dcd3-117">Многие поставщиками адресной книги не поддерживают уведомлений на их сообщениями пользователей и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="1dcd3-118">Уведомления о таблице являются достаточными для отслеживания изменений и сообщения о них для пользователей.</span><span class="sxs-lookup"><span data-stu-id="1dcd3-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

