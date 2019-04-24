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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299505"
---
# <a name="handing-address-book-notification"></a><span data-ttu-id="077ee-103">Обработка уведомления об адресной книге</span><span class="sxs-lookup"><span data-stu-id="077ee-103">Handing address book notification</span></span>
  
<span data-ttu-id="077ee-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="077ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="077ee-105">Уведомления в адресной книге позволяют клиенту получать сведения о событиях, происходящих с любой записью адресной книги или конкретной записи.</span><span class="sxs-lookup"><span data-stu-id="077ee-105">Address book notifications allow a client to learn of events that occur to any address book entry or to a particular entry.</span></span> <span data-ttu-id="077ee-106">Вы можете зарегистрироваться для получения этих уведомлений либо через адресную книгу MAPI, вызвав [IAddrBook:: Advise](iaddrbook-advise.md) или через иерархию или таблицу содержимого контейнера адресной книги, вызывая метод [IMAPITable:: Advise](imapitable-advise.md).</span><span class="sxs-lookup"><span data-stu-id="077ee-106">You can register for these notifications either through the MAPI address book by calling [IAddrBook::Advise](iaddrbook-advise.md) or through an address book container's hierarchy or contents table by calling [IMAPITable::Advise](imapitable-advise.md).</span></span> 
  
<span data-ttu-id="077ee-107">Указание идентификатора записи для контейнера адресной книги, списка рассылки или пользователя обмена сообщениями, если вы регистрируете уведомления для конкретной записи и имеет значение NULL, если регистрация для получения уведомлений для всей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="077ee-107">Specify the entry identifier of an address book container, distribution list, or messaging user if you are registering for notifications on a particular entry and NULL if registering for notifications on the entire address book.</span></span> <span data-ttu-id="077ee-108">Идентификатор записи должен представлять пользователя или список рассылки системы обмена сообщениями в контейнере адресной книги.</span><span class="sxs-lookup"><span data-stu-id="077ee-108">The entry identifier must represent a messaging user or distribution list in an address book container.</span></span> <span data-ttu-id="077ee-109">**IAddrBook:: Advise** проверяет этот идентификатор записи, чтобы определить, какой поставщик адресных книг отвечает за соответствующий объект, и перенаправит вызов соответствующему поставщику адресной книги метод [Иаблогон:: Advise](iablogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="077ee-109">**IAddrBook::Advise** examines this entry identifier to determine which address book provider is responsible for the corresponding object and forwards the call to the appropriate address book provider's [IABLogon::Advise](iablogon-advise.md) method.</span></span> 
  
<span data-ttu-id="077ee-110">Клиенты могут регистрировать события следующих типов в записях адресной книги:</span><span class="sxs-lookup"><span data-stu-id="077ee-110">Clients can register for the following types of events on address book entries:</span></span>
  
- <span data-ttu-id="077ee-111">Критическая ошибка</span><span class="sxs-lookup"><span data-stu-id="077ee-111">Critical error</span></span>
    
- <span data-ttu-id="077ee-112">Любые события объектов (созданные, измененные, удаленные, перемещенные или скопированные);</span><span class="sxs-lookup"><span data-stu-id="077ee-112">Any of the object events (created, modified, deleted, moved, or copied)</span></span>
    
- <span data-ttu-id="077ee-113">Измененная таблица</span><span class="sxs-lookup"><span data-stu-id="077ee-113">Table modified</span></span>
    
<span data-ttu-id="077ee-114">Как правило, регистрация выполняется только для содержимого контейнера адресной книги и таблиц иерархий.</span><span class="sxs-lookup"><span data-stu-id="077ee-114">Typically, registration occurs only on address book container contents and hierarchy tables.</span></span> <span data-ttu-id="077ee-115">Клиенты иногда регистрируются с объектами сообщений нижнего уровня и списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="077ee-115">It is rare that clients register with the lower level messaging user and distribution list objects.</span></span> <span data-ttu-id="077ee-116">Это обусловлено тем, что:</span><span class="sxs-lookup"><span data-stu-id="077ee-116">This is because:</span></span>
  
- <span data-ttu-id="077ee-117">Многие поставщики адресных книг не поддерживают уведомления для пользователей системы обмена сообщениями и списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="077ee-117">Many address book providers do not support notifications on their messaging users and distribution lists.</span></span>
    
- <span data-ttu-id="077ee-118">Для отслеживания изменений и отправки отчетов пользователям достаточно уведомлений таблицы.</span><span class="sxs-lookup"><span data-stu-id="077ee-118">Table notifications are sufficient for tracking changes and reporting them to users.</span></span>
    

