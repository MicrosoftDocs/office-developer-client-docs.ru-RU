---
title: Добавление записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421342"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="73ae5-103">Добавление записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="73ae5-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="73ae5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73ae5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73ae5-105">Чтобы добавить пользователя обмена сообщениями или список рассылки в контейнер, клиент вызывает [IAddrBook::NewEntry](iaddrbook-newentry.md) или поставщик вызывает [IMAPISupport::NewEntry](imapisupport-newentry.md) с идентификатором входа целевого контейнера в параметре _lpEIDContainer._</span><span class="sxs-lookup"><span data-stu-id="73ae5-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="73ae5-106">MAPI, в свою очередь, вызывает метод [IABContainer::CreateEntry](iabcontainer-createentry.md) для создания записи с помощью разового шаблона из разовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="73ae5-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="73ae5-107">Разовая шаблона позволяет клиенту создать нового получателя определенного типа.</span><span class="sxs-lookup"><span data-stu-id="73ae5-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="73ae5-108">Большинство полей можно изменить.</span><span class="sxs-lookup"><span data-stu-id="73ae5-108">Most of the fields are editable.</span></span> <span data-ttu-id="73ae5-109">Шаблон, на который указывает параметр  _lpEntryID,_ может быть шаблоном, который поставщик поставляет или может быть шаблоном от иностранного поставщика, если поставщик поддерживает иностранные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="73ae5-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="73ae5-110">Реализация **CreateEntry для** поставщиков, которые могут создавать получателей из иностранного шаблона, всегда сложнее реализации для поставщиков, которые не могут.</span><span class="sxs-lookup"><span data-stu-id="73ae5-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="73ae5-111">**Реализация IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="73ae5-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="73ae5-112">Определите тип идентификатора записи, заданного _параметром lpEntryID._</span><span class="sxs-lookup"><span data-stu-id="73ae5-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="73ae5-113">Если идентификатор записи представляет шаблон для пользователя обмена сообщениями, списка рассылки или контейнера адресной книги, который принадлежит поставщику:</span><span class="sxs-lookup"><span data-stu-id="73ae5-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="73ae5-114">Создание и инициализация соответствующего объекта.</span><span class="sxs-lookup"><span data-stu-id="73ae5-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="73ae5-115">При желании поставщик может установить некоторые начальные свойства.</span><span class="sxs-lookup"><span data-stu-id="73ae5-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="73ae5-116">Эти свойства зависят от типа создаемого получателя.</span><span class="sxs-lookup"><span data-stu-id="73ae5-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="73ae5-117">Верни указатель на реализацию объекта в содержимом параметра _lppMAPIPropEntry._</span><span class="sxs-lookup"><span data-stu-id="73ae5-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="73ae5-118">Если идентификатор записи представляет шаблон для иностранного поставщика:</span><span class="sxs-lookup"><span data-stu-id="73ae5-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="73ae5-119">Вызов [IMAPISupport::OpenEntry,](imapisupport-openentry.md) чтобы открыть иностранный объект.</span><span class="sxs-lookup"><span data-stu-id="73ae5-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="73ae5-120">Чтобы получить его свойства, позвоните по методу [IMAPIProp::GetProps,](imapiprop-getprops.md) передав NULL для массива тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="73ae5-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="73ae5-121">Изменение массива значений свойств, возвращаемого **из GetProps,** изменив тег свойства на PR_NULL для всех свойств, которые не будут применяться к новому объекту и не должны быть переданы.</span><span class="sxs-lookup"><span data-stu-id="73ae5-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="73ae5-122">Создайте идентификатор входа для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="73ae5-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="73ae5-123">Создание нового объекта соответствующего типа, пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="73ae5-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="73ae5-124">Инициализация нового объекта путем установки свойств по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="73ae5-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="73ae5-125">Проверьте, поддерживает ли иностранный объект **свойство PR_TEMPLATEID** [(PidTagTemplateid).](pidtagtemplateid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="73ae5-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="73ae5-126">Если иностранный объект поддерживает **PR_TEMPLATEID,** позвоните по телефону [IMAPISupport::OpenTemplateID,](imapisupport-opentemplateid.md) чтобы получить интерфейс объекта свойства у иностранного поставщика и задать содержимое параметра  _lppMAPIPropEntry_ для реализации объекта зарубежного свойства.</span><span class="sxs-lookup"><span data-stu-id="73ae5-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="73ae5-127">Если иностранный объект не поддерживает **PR_TEMPLATEID,** установите содержимое параметра  _lppMAPIPropEntry_ для реализации нового объекта поставщиком.</span><span class="sxs-lookup"><span data-stu-id="73ae5-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="73ae5-128">Вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) объекта, на который указывает параметр  _lppMAPIPropEntry,_ чтобы задать соответствующие свойства от внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="73ae5-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

