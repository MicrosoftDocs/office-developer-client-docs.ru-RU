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
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="5bd3c-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5bd3c-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="5bd3c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bd3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bd3c-105">Поддерживает доступ к адресной книге MAPI и включает такие операции, как отображение общих диалоговых окон; открывающие контейнеры, пользователи обмена сообщениями и списки рассылки; и выполнение разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bd3c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5bd3c-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="5bd3c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="5bd3c-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="5bd3c-109">Объекты адресной книги</span><span class="sxs-lookup"><span data-stu-id="5bd3c-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="5bd3c-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bd3c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="5bd3c-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="5bd3c-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-112">Called by:</span></span>  <br/> |<span data-ttu-id="5bd3c-113">Клиентские приложения, поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="5bd3c-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="5bd3c-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5bd3c-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="5bd3c-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="5bd3c-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="5bd3c-117">лпадрбук</span><span class="sxs-lookup"><span data-stu-id="5bd3c-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="5bd3c-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="5bd3c-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="5bd3c-119">Недоступно для записи</span><span class="sxs-lookup"><span data-stu-id="5bd3c-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5bd3c-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="5bd3c-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5bd3c-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="5bd3c-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="5bd3c-122">Открывает запись адресной книги и возвращает указатель на интерфейс, который можно использовать для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="5bd3c-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="5bd3c-124">Сравнивает два идентификатора записи, которые относятся к определенному поставщику адресных книг, чтобы определить, ссылаются ли они на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-125">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="5bd3c-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="5bd3c-126">Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях в одной или нескольких записях в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="5bd3c-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="5bd3c-128">Отменяет регистрацию уведомления, установленную ранее для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-129">креатеонеофф</span><span class="sxs-lookup"><span data-stu-id="5bd3c-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="5bd3c-130">Создает идентификатор записи для одного адреса.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-131">невентри</span><span class="sxs-lookup"><span data-stu-id="5bd3c-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="5bd3c-132">Добавляет нового получателя в контейнер адресной книги или в список получателей исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="5bd3c-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="5bd3c-134">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-135">Address</span><span class="sxs-lookup"><span data-stu-id="5bd3c-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="5bd3c-136">Отображает диалоговое окно "Адресная книга Outlook".</span><span class="sxs-lookup"><span data-stu-id="5bd3c-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-137">Details</span><span class="sxs-lookup"><span data-stu-id="5bd3c-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="5bd3c-138">Отображает диалоговое окно, в котором отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="5bd3c-139">**реЦипоптионс**</span><span class="sxs-lookup"><span data-stu-id="5bd3c-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="5bd3c-140">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="5bd3c-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="5bd3c-141">**куеридефаултреЦипопт**</span><span class="sxs-lookup"><span data-stu-id="5bd3c-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="5bd3c-142">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="5bd3c-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-143">жетпаб</span><span class="sxs-lookup"><span data-stu-id="5bd3c-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="5bd3c-144">Возвращает идентификатор элемента контейнера, назначенный в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="5bd3c-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-145">сетпаб</span><span class="sxs-lookup"><span data-stu-id="5bd3c-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="5bd3c-146">Назначает определенный контейнер в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="5bd3c-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-147">жетдефаултдир</span><span class="sxs-lookup"><span data-stu-id="5bd3c-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="5bd3c-148">Возвращает идентификатор для исходного контейнера адресных книг.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-149">сетдефаултдир</span><span class="sxs-lookup"><span data-stu-id="5bd3c-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="5bd3c-150">Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию, который изначально становится доступным.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-151">жетсеарчпас</span><span class="sxs-lookup"><span data-stu-id="5bd3c-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="5bd3c-152">Возвращает упорядоченный список идентификаторов элементов контейнеров, которые должны быть включены в процесс разрешения имен, инициированный методом [ресолвенаме](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="5bd3c-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-153">сетсеарчпас</span><span class="sxs-lookup"><span data-stu-id="5bd3c-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="5bd3c-154">Задает новый путь поиска в профиле, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="5bd3c-155">препаререЦипс</span><span class="sxs-lookup"><span data-stu-id="5bd3c-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="5bd3c-156">Подготавливает список получателей для последующего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="5bd3c-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bd3c-157">См. также</span><span class="sxs-lookup"><span data-stu-id="5bd3c-157">See also</span></span>



[<span data-ttu-id="5bd3c-158">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5bd3c-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

