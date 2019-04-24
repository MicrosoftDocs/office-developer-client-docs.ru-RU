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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331880"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="8a45d-103">Добавление записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="8a45d-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="8a45d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a45d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a45d-105">Чтобы добавить пользователя или список рассылки для обмена сообщениями в контейнер, клиент вызывает [IAddrBook:: невентри](iaddrbook-newentry.md) или поставщик вызывает [Имаписуппорт:: невентри](imapisupport-newentry.md) с идентификатором записи целевого контейнера в параметре _лпеидконтаинер_ .</span><span class="sxs-lookup"><span data-stu-id="8a45d-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="8a45d-106">В свою очередь MAPI вызывает метод контейнера [иабконтаинер:: креатинтри](iabcontainer-createentry.md) , чтобы создать запись с помощью одноразового шаблона из одноразовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="8a45d-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="8a45d-107">Одноразовый шаблон позволяет клиенту создавать нового получателя определенного типа.</span><span class="sxs-lookup"><span data-stu-id="8a45d-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="8a45d-108">Большинство полей можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="8a45d-108">Most of the fields are editable.</span></span> <span data-ttu-id="8a45d-109">Шаблоном, на который указывает параметр _лпентрид_ , может быть один, который поставщик предоставил или может быть шаблоном от внешнего поставщика, если ваш поставщик поддерживает внешние шаблоны.</span><span class="sxs-lookup"><span data-stu-id="8a45d-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="8a45d-110">Реализации **креатинтри** для поставщиков, которые могут создавать получателей из внешнего шаблона, всегда более сложны, чем реализации для поставщиков, которые не могут.</span><span class="sxs-lookup"><span data-stu-id="8a45d-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="8a45d-111">**Реализация Иабконтаинер:: Креатинтри**</span><span class="sxs-lookup"><span data-stu-id="8a45d-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="8a45d-112">Определите тип идентификатора записи, заданный параметром _лпентрид_ .</span><span class="sxs-lookup"><span data-stu-id="8a45d-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="8a45d-113">Если идентификатор записи представляет шаблон для пользователя обмена сообщениями, списка рассылки или контейнера адресной книги, принадлежащего поставщику:</span><span class="sxs-lookup"><span data-stu-id="8a45d-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="8a45d-114">Создайте и инициализируйте соответствующий объект.</span><span class="sxs-lookup"><span data-stu-id="8a45d-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="8a45d-115">При необходимости поставщик может задать некоторые начальные свойства.</span><span class="sxs-lookup"><span data-stu-id="8a45d-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="8a45d-116">Эти свойства зависят от типа создаваемого получателя.</span><span class="sxs-lookup"><span data-stu-id="8a45d-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="8a45d-117">Возвращает указатель на реализацию объекта в содержимом параметра _лппмапипропентри_ .</span><span class="sxs-lookup"><span data-stu-id="8a45d-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="8a45d-118">Если идентификатор записи представляет шаблон для внешнего поставщика:</span><span class="sxs-lookup"><span data-stu-id="8a45d-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="8a45d-119">Call [имаписуппорт:: OpenEntry](imapisupport-openentry.md) , чтобы открыть внешний объект.</span><span class="sxs-lookup"><span data-stu-id="8a45d-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="8a45d-120">ВыЗовите метод [IMAPIProp::](imapiprop-getprops.md) /PROPS объекта, ПЕРЕДАВ значение NULL для массива тегов свойств, чтобы получить его свойства.</span><span class="sxs-lookup"><span data-stu-id="8a45d-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="8a45d-121">Измените массив значений свойства, возвращаемый \*\*\*\* методом Props, изменив тег свойства на пр_нулл для всех свойств, которые не будут применяться к новому объекту и не должны передаваться.</span><span class="sxs-lookup"><span data-stu-id="8a45d-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="8a45d-122">Создание идентификатора записи для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="8a45d-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="8a45d-123">Создайте новый объект соответствующего типа: "пользователь обмена сообщениями" или "список рассылки".</span><span class="sxs-lookup"><span data-stu-id="8a45d-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="8a45d-124">Инициализируйте новый объект, устанавливая свойства по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8a45d-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="8a45d-125">Проверьте, поддерживает ли внешний объект свойство **пр_темплатеид** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8a45d-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="8a45d-126">Если внешний объект поддерживает **пр_темплатеид**, вызовите [Имаписуппорт:: опентемплатеид](imapisupport-opentemplateid.md) , чтобы получить интерфейс объекта свойства из внешнего поставщика и присвоить параметру _лппмапипропентри_ значение Foreign Property. Реализация объекта.</span><span class="sxs-lookup"><span data-stu-id="8a45d-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="8a45d-127">Если внешний объект не поддерживает **пр_темплатеид**, задайте значение параметра _лппмапипропентри_ для реализации поставщика нового объекта.</span><span class="sxs-lookup"><span data-stu-id="8a45d-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="8a45d-128">ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) объекта, на который указывает параметр _лппмапипропентри_ , чтобы задать соответствующие свойства из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="8a45d-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

