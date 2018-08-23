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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590136"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="21422-103">Добавление записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="21422-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="21422-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21422-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21422-105">Чтобы добавить обмена сообщениями пользователя или список рассылки в контейнер, вызовы клиента [IAddrBook::NewEntry](iaddrbook-newentry.md) или поставщиком вызывает [IMAPISupport::NewEntry](imapisupport-newentry.md) с идентификатором записи конечного контейнера с помощью параметра _lpEIDContainer_ .</span><span class="sxs-lookup"><span data-stu-id="21422-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="21422-106">MAPI в свою очередь вызывает метод [IABContainer::CreateEntry](iabcontainer-createentry.md) контейнера для создания записи, с помощью шаблона одноразовых из одноразовых таблицы.</span><span class="sxs-lookup"><span data-stu-id="21422-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="21422-107">Шаблон одноразовых позволяет клиентским для создания нового получателя определенного типа.</span><span class="sxs-lookup"><span data-stu-id="21422-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="21422-108">Большая часть поля доступны для редактирования.</span><span class="sxs-lookup"><span data-stu-id="21422-108">Most of the fields are editable.</span></span> <span data-ttu-id="21422-109">Шаблон, на который указывает параметр _lpEntryID_ может быть, которая предоставляет поставщик или может быть шаблон от внешнего поставщика, если поставщик поддерживает внешнего шаблонов.</span><span class="sxs-lookup"><span data-stu-id="21422-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="21422-110">Реализации **CreateEntry** для поставщиков, которые можно создать получателей из внешнего шаблона всегда являются более сложным, чем реализации для поставщиков, которые невозможно.</span><span class="sxs-lookup"><span data-stu-id="21422-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="21422-111">**Для реализации IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="21422-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="21422-112">Определение типа записи идентификатор, указанный в параметре _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="21422-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="21422-113">Если идентификатор записи представляет шаблон для обмена сообщениями пользователя, список рассылки или контейнер адресной книги, принадлежащие к поставщику:</span><span class="sxs-lookup"><span data-stu-id="21422-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="21422-114">Создание и инициализация подходящий объект.</span><span class="sxs-lookup"><span data-stu-id="21422-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="21422-115">При желании к поставщику можно задать некоторые начальные свойства.</span><span class="sxs-lookup"><span data-stu-id="21422-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="21422-116">Эти свойства зависят от типа создаваемого получателя.</span><span class="sxs-lookup"><span data-stu-id="21422-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="21422-117">Возвращает указатель для реализации объекта в содержимое для параметра _lppMAPIPropEntry_ .</span><span class="sxs-lookup"><span data-stu-id="21422-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="21422-118">Если идентификатор записи представляет шаблон для внешнего поставщика:</span><span class="sxs-lookup"><span data-stu-id="21422-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="21422-119">Вызовите [IMAPISupport::OpenEntry](imapisupport-openentry.md) , чтобы открыть внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="21422-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="21422-120">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) объекта, передав значение NULL для массива тега свойства, чтобы получить его свойства.</span><span class="sxs-lookup"><span data-stu-id="21422-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="21422-121">Изменение массива значение свойства, возвращенные **GetProps** изменяя тег свойства PR_NULL для всех свойств, которые не будут применяться к новому объекту и не должны быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="21422-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="21422-122">Создайте запись идентификатор для этого нового объекта.</span><span class="sxs-lookup"><span data-stu-id="21422-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="21422-123">Создание объекта соответствующего типа, либо обмена сообщениями пользователя или списку рассылки.</span><span class="sxs-lookup"><span data-stu-id="21422-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="21422-124">Инициализируйте новый объект путем установки свойства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="21422-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="21422-125">Проверьте, поддерживает ли внешний объект свойство **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="21422-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="21422-126">Если внешний объект поддерживает **PR_TEMPLATEID**, вызовите [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) для извлечения интерфейса объекта свойство от внешнего поставщика и задать содержимое параметра _lppMAPIPropEntry_ внешнего свойства Реализация объекта.</span><span class="sxs-lookup"><span data-stu-id="21422-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="21422-127">Если внешний объект не поддерживает **PR_TEMPLATEID**, необходимо задайте содержимое параметра _lppMAPIPropEntry_ для реализации поставщика нового объекта.</span><span class="sxs-lookup"><span data-stu-id="21422-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="21422-128">Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) объект, указанный с помощью параметра _lppMAPIPropEntry_ , чтобы задать соответствующие свойства из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="21422-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

