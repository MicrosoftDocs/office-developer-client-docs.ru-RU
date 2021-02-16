---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da71e9dd5f2fc20bb1daf528f4466ea29507bf06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429826"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="b96db-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b96db-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="b96db-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b96db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b96db-105">Поддерживает доступ к адресной книге MAPI и включает такие операции, как отображение общих диалогов; открытие контейнеров, пользователей сообщений и списков рассылки; и разрешение имен.</span><span class="sxs-lookup"><span data-stu-id="b96db-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b96db-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b96db-106">Header file:</span></span>  <br/> |<span data-ttu-id="b96db-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b96db-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b96db-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="b96db-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b96db-109">Объекты адресной книги</span><span class="sxs-lookup"><span data-stu-id="b96db-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="b96db-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b96db-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b96db-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b96db-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b96db-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b96db-112">Called by:</span></span>  <br/> |<span data-ttu-id="b96db-113">Клиентские приложения, поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="b96db-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="b96db-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b96db-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b96db-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="b96db-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="b96db-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b96db-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b96db-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="b96db-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="b96db-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="b96db-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="b96db-119">Не подавно</span><span class="sxs-lookup"><span data-stu-id="b96db-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b96db-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="b96db-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b96db-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b96db-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="b96db-122">Открывает запись адресной книги и возвращает указатель на интерфейс, который можно использовать для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="b96db-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="b96db-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b96db-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="b96db-124">Сравнивает два идентификатора записей, принадлежащих конкретному поставщику адресной книги, чтобы определить, относятся ли они к одному объекту адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b96db-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="b96db-125">Консультация</span><span class="sxs-lookup"><span data-stu-id="b96db-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="b96db-126">Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях одной или более записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b96db-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="b96db-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="b96db-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="b96db-128">Отменяет регистрацию уведомлений, ранее установленную для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b96db-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="b96db-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b96db-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="b96db-130">Создает идентификатор записи для разовый адрес.</span><span class="sxs-lookup"><span data-stu-id="b96db-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="b96db-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="b96db-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="b96db-132">Добавляет нового получателя в контейнер адресной книги или в список получателей исходяного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b96db-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="b96db-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="b96db-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="b96db-134">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="b96db-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="b96db-135">Address</span><span class="sxs-lookup"><span data-stu-id="b96db-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="b96db-136">Отображает диалоговое окно адресной книги Outlook.</span><span class="sxs-lookup"><span data-stu-id="b96db-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="b96db-137">Details</span><span class="sxs-lookup"><span data-stu-id="b96db-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="b96db-138">Отображает диалоговое окно с подробными сведениями об определенной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b96db-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="b96db-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="b96db-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="b96db-140">*Не поддерживается и не документируется.*</span><span class="sxs-lookup"><span data-stu-id="b96db-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="b96db-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="b96db-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="b96db-142">*Не поддерживается и не документируется.*</span><span class="sxs-lookup"><span data-stu-id="b96db-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="b96db-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="b96db-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="b96db-144">Возвращает идентификатор записи контейнера, назначенного в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="b96db-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b96db-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="b96db-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="b96db-146">Назначает определенный контейнер в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="b96db-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b96db-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b96db-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="b96db-148">Возвращает идентификатор записи для исходного контейнера адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b96db-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="b96db-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b96db-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="b96db-150">Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию, который изначально был доступен.</span><span class="sxs-lookup"><span data-stu-id="b96db-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="b96db-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b96db-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="b96db-152">Возвращает упорядоченный список идентификаторов записей контейнеров, которые необходимо включить в процесс разрешения имен, инициированный методом [ResolveName.](iaddrbook-resolvename.md)</span><span class="sxs-lookup"><span data-stu-id="b96db-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="b96db-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b96db-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="b96db-154">Задает новый путь поиска в профиле, используемый для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="b96db-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="b96db-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="b96db-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="b96db-156">Подготавливает список получателей к дальнейшему использованию системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b96db-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b96db-157">См. также</span><span class="sxs-lookup"><span data-stu-id="b96db-157">See also</span></span>



[<span data-ttu-id="b96db-158">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b96db-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

