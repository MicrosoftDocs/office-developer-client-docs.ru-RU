---
title: Обработка уведомления об адресной книге
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413537"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="16a47-103">Обработка уведомления об адресной книге</span><span class="sxs-lookup"><span data-stu-id="16a47-103">Handing address book notification</span></span>
  
<span data-ttu-id="16a47-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16a47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16a47-105">Уведомления адресной книги позволяют клиенту узнать о событиях, которые происходят с любой записью адресной книги или определенной записью.</span><span class="sxs-lookup"><span data-stu-id="16a47-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="16a47-106">Вы можете зарегистрироваться для этих уведомлений либо через адресную книгу MAPI, позвонив [в IAddrBook:::Advise](iaddrbook-advise.md) или через иерархию контейнера адресной книги или таблицу содержимого, позвонив [в IMAPITable::Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="16a47-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="16a47-107">Укажите идентификатор входа контейнера адресной книги, списка рассылки или пользователя обмена сообщениями, если вы регистрируете уведомления по определенной записи и NULL, если регистрируете уведомления во всей адресной книге.</span><span class="sxs-lookup"><span data-stu-id="16a47-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="16a47-108">Идентификатор записи должен представлять пользователя обмена сообщениями или список рассылки в контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="16a47-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="16a47-109">**IAddrBook::Advise** проверяет этот идентификатор записи, чтобы определить, какой поставщик адресной книги отвечает за соответствующий объект, и передает вызов в метод [IABLogon::Advise](iablogon-advise.md) соответствующего поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="16a47-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="16a47-110">Клиенты могут зарегистрироваться для следующих типов событий в записях адресной книги:</span><span class="sxs-lookup"><span data-stu-id="16a47-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="16a47-111">Критическая ошибка</span><span class="sxs-lookup"><span data-stu-id="16a47-111">Critical error</span></span>
    
- <span data-ttu-id="16a47-112">Любые события объекта (созданные, измененные, удаленные, перенесенные или скопированные)</span><span class="sxs-lookup"><span data-stu-id="16a47-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="16a47-113">Изменена таблица</span><span class="sxs-lookup"><span data-stu-id="16a47-113">Table modified</span></span>
    
<span data-ttu-id="16a47-114">Как правило, регистрация происходит только в содержимого контейнера адресной книги и таблицах иерархии.</span><span class="sxs-lookup"><span data-stu-id="16a47-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="16a47-115">Редко клиенты регистрируются с объектами пользователей сообщений более низкого уровня и объектов списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="16a47-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="16a47-116">Это потому, что:</span><span class="sxs-lookup"><span data-stu-id="16a47-116">This is because:</span></span>
  
- <span data-ttu-id="16a47-117">Многие поставщики адресных книг не поддерживают уведомления в своих пользователях сообщений и списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="16a47-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="16a47-118">Уведомлений в таблице достаточно для отслеживания изменений и их отчетности пользователям.</span><span class="sxs-lookup"><span data-stu-id="16a47-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

