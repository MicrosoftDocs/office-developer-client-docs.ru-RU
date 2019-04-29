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
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="c3d64-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c3d64-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="c3d64-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d64-105">Поддерживает доступ к адресной книге MAPI и включает такие операции, как отображение общих диалоговых окон; открывающие контейнеры, пользователи обмена сообщениями и списки рассылки; и выполнение разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="c3d64-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3d64-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c3d64-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3d64-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="c3d64-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c3d64-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="c3d64-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="c3d64-109">Объекты адресной книги</span><span class="sxs-lookup"><span data-stu-id="c3d64-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="c3d64-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c3d64-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3d64-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d64-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="c3d64-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c3d64-112">Called by:</span></span>  <br/> |<span data-ttu-id="c3d64-113">Клиентские приложения, поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c3d64-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="c3d64-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c3d64-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c3d64-115">Иид_иаддрбук</span><span class="sxs-lookup"><span data-stu-id="c3d64-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="c3d64-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="c3d64-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="c3d64-117">ЛПАДРБУК</span><span class="sxs-lookup"><span data-stu-id="c3d64-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="c3d64-118">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="c3d64-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="c3d64-119">Недоступно для записи</span><span class="sxs-lookup"><span data-stu-id="c3d64-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c3d64-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="c3d64-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c3d64-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c3d64-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="c3d64-122">Открывает запись адресной книги и возвращает указатель на интерфейс, который можно использовать для доступа к записи.</span><span class="sxs-lookup"><span data-stu-id="c3d64-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="c3d64-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="c3d64-124">Сравнивает два идентификатора записи, которые относятся к определенному поставщику адресных книг, чтобы определить, ссылаются ли они на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c3d64-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-125">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="c3d64-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="c3d64-126">Регистрирует клиента или поставщика услуг для получения уведомлений об изменениях в одной или нескольких записях в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="c3d64-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="c3d64-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="c3d64-128">ОтМеняет регистрацию уведомления, установленную ранее для записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c3d64-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-129">Креатеонеофф</span><span class="sxs-lookup"><span data-stu-id="c3d64-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="c3d64-130">Создает идентификатор записи для одного адреса.</span><span class="sxs-lookup"><span data-stu-id="c3d64-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-131">Невентри</span><span class="sxs-lookup"><span data-stu-id="c3d64-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="c3d64-132">Добавляет нового получателя в контейнер адресной книги или в список получателей исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="c3d64-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="c3d64-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="c3d64-134">Выполняет разрешение имен, назначая идентификаторы записей получателям в списке получателей.</span><span class="sxs-lookup"><span data-stu-id="c3d64-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-135">Address</span><span class="sxs-lookup"><span data-stu-id="c3d64-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="c3d64-136">Отображает диалоговое окно "Адресная книга Outlook".</span><span class="sxs-lookup"><span data-stu-id="c3d64-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="c3d64-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="c3d64-138">Отображает диалоговое окно, в котором отображаются сведения о конкретной записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c3d64-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="c3d64-139">**РеЦипоптионс**</span><span class="sxs-lookup"><span data-stu-id="c3d64-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="c3d64-140">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="c3d64-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="c3d64-141">**КуеридефаултреЦипопт**</span><span class="sxs-lookup"><span data-stu-id="c3d64-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="c3d64-142">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="c3d64-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="c3d64-143">Жетпаб</span><span class="sxs-lookup"><span data-stu-id="c3d64-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="c3d64-144">Возвращает идентификатор элемента контейнера, назначенный в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="c3d64-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="c3d64-145">Сетпаб</span><span class="sxs-lookup"><span data-stu-id="c3d64-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="c3d64-146">Назначает определенный контейнер в качестве личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="c3d64-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="c3d64-147">Жетдефаултдир</span><span class="sxs-lookup"><span data-stu-id="c3d64-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="c3d64-148">Возвращает идентификатор для исходного контейнера адресных книг.</span><span class="sxs-lookup"><span data-stu-id="c3d64-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-149">Сетдефаултдир</span><span class="sxs-lookup"><span data-stu-id="c3d64-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="c3d64-150">Устанавливает указанный контейнер в качестве контейнера адресной книги по умолчанию, который изначально становится доступным.</span><span class="sxs-lookup"><span data-stu-id="c3d64-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-151">Жетсеарчпас</span><span class="sxs-lookup"><span data-stu-id="c3d64-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="c3d64-152">Возвращает упорядоченный список идентификаторов элементов контейнеров, которые должны быть включены в процесс разрешения имен, инициированный методом [ресолвенаме](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d64-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-153">Сетсеарчпас</span><span class="sxs-lookup"><span data-stu-id="c3d64-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="c3d64-154">Задает новый путь поиска в профиле, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="c3d64-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="c3d64-155">ПрепаререЦипс</span><span class="sxs-lookup"><span data-stu-id="c3d64-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="c3d64-156">ПодГотавливает список получателей для последующего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c3d64-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c3d64-157">См. также</span><span class="sxs-lookup"><span data-stu-id="c3d64-157">See also</span></span>



[<span data-ttu-id="c3d64-158">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="c3d64-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

