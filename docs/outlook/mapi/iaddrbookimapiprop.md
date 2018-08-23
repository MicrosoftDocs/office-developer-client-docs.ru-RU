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
ms.openlocfilehash: 44bc6de420953bd665bd3caa336b76b15c1effd6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579461"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="cf08b-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cf08b-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="cf08b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf08b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf08b-105">Поддерживает доступ к адресной книге MAPI, а также операции, такие как отображение общие диалоговые окна; Открытие контейнеров, системы обмена сообщениями пользователей и списки рассылки; и разрешение имен для выполнения.</span><span class="sxs-lookup"><span data-stu-id="cf08b-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf08b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cf08b-106">Header file:</span></span>  <br/> |<span data-ttu-id="cf08b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="cf08b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="cf08b-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="cf08b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cf08b-109">Объекты адресной книги</span><span class="sxs-lookup"><span data-stu-id="cf08b-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="cf08b-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="cf08b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cf08b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="cf08b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="cf08b-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="cf08b-112">Called by:</span></span>  <br/> |<span data-ttu-id="cf08b-113">Клиентские приложения, поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="cf08b-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="cf08b-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="cf08b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cf08b-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="cf08b-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="cf08b-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="cf08b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="cf08b-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="cf08b-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="cf08b-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="cf08b-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="cf08b-119">Не для записи</span><span class="sxs-lookup"><span data-stu-id="cf08b-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cf08b-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="cf08b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cf08b-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="cf08b-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="cf08b-122">Открывает запись книги и возвращает указатель на интерфейс, который можно использовать для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="cf08b-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cf08b-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="cf08b-124">Сравнение двух идентификаторы записей, относящихся к конкретной адресной книге, чтобы определить, является ли они ссылаются на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cf08b-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-125">Уведомить</span><span class="sxs-lookup"><span data-stu-id="cf08b-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="cf08b-126">Регистрация клиента или поставщика для получения уведомлений об изменениях в одну или несколько записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="cf08b-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="cf08b-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="cf08b-128">Отмена регистрации уведомлений, ранее созданные записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cf08b-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="cf08b-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="cf08b-130">Создает запись идентификатор указывает адрес.</span><span class="sxs-lookup"><span data-stu-id="cf08b-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="cf08b-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="cf08b-132">Добавляет нового получателя контейнер адресной книги или списка получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf08b-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="cf08b-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="cf08b-134">Выполняет разрешение имен, назначение идентификаторов запись для получателей в список получателей.</span><span class="sxs-lookup"><span data-stu-id="cf08b-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-135">Адрес</span><span class="sxs-lookup"><span data-stu-id="cf08b-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="cf08b-136">Отображает диалоговое окно Outlook адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cf08b-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="cf08b-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="cf08b-138">Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cf08b-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="cf08b-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="cf08b-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="cf08b-140">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="cf08b-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="cf08b-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="cf08b-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="cf08b-142">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="cf08b-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="cf08b-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="cf08b-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="cf08b-144">Возвращает идентификатор записи контейнера, который используется в качестве Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="cf08b-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="cf08b-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="cf08b-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="cf08b-146">Назначает конкретным контейнером Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="cf08b-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="cf08b-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="cf08b-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="cf08b-148">Возвращает идентификатор записи для контейнер начальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cf08b-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="cf08b-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="cf08b-150">Устанавливает указанный контейнер как контейнер адресной книги по умолчанию, который изначально становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="cf08b-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cf08b-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="cf08b-152">Возвращает упорядоченный список идентификаторов запись контейнеров, которые будут включены в процесс разрешения имен, инициированных метод [ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="cf08b-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="cf08b-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="cf08b-154">Задает новый путь для поиска профиля, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="cf08b-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="cf08b-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="cf08b-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="cf08b-156">Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cf08b-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf08b-157">См. также</span><span class="sxs-lookup"><span data-stu-id="cf08b-157">See also</span></span>



[<span data-ttu-id="cf08b-158">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="cf08b-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

