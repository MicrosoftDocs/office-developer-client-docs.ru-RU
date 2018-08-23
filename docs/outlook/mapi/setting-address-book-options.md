---
title: Установка параметров адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0d93fde7d654f0ee56dcda9f2fb69ad622e476dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593622"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="61e6f-103">Установка параметров адресной книги</span><span class="sxs-lookup"><span data-stu-id="61e6f-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="61e6f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61e6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61e6f-105">Можно задать три свойства, описывающие параметры для использования в адресной книге:</span><span class="sxs-lookup"><span data-stu-id="61e6f-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="61e6f-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61e6f-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="61e6f-107">Свойство **PR_AB_SEARCH_PATH** используется [IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров для принимать участие в том порядке, в том, что они должны принимать участие и разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="61e6f-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="61e6f-108">Для каждого контейнера в **PR_AB_SEARCH_PATH** **IAddrBook::ResolveName** вызывает метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="61e6f-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="61e6f-109">Контейнеры в начале **PR_AB_SEARCH_PATH** выполняется перед контейнеров в конце **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="61e6f-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="61e6f-110">Порядок поиска в **PR_AB_SEARCH_PATH** задается с помощью структуру [SRowSet](srowset.md) ту же структуру, которая используется для представления строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="61e6f-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="61e6f-111">Можно просмотреть текущий путь поиска путем вызова метода [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и измените его путем вызова метода [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) .</span><span class="sxs-lookup"><span data-stu-id="61e6f-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="61e6f-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61e6f-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="61e6f-113">Свойство **PR_AB_DEFAULT_DIR** — это идентификатор операции контейнер адресной книги для отображения изначально при отображении в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="61e6f-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="61e6f-114">Каталог по умолчанию действует, пока не будет изменено путем вызова метода [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="61e6f-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="61e6f-115">Можно просматривать каталог по умолчанию путем вызова метода [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="61e6f-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="61e6f-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61e6f-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="61e6f-117">Эти три свойства являются особыми, так как он не может работать с ними с помощью стандартных способов **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="61e6f-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="61e6f-118">Вместо этого необходимо использовать методы **IAddrBook** .</span><span class="sxs-lookup"><span data-stu-id="61e6f-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="61e6f-119">Так как ни один из этих свойств можно изменить с помощью **IMAPIProp::SetProps**, нет необходимости для вызова **IMAPIProp::SaveChanges** вносить изменения постоянной.</span><span class="sxs-lookup"><span data-stu-id="61e6f-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="61e6f-120">Изменения, сделанные через методы **IAddrBook** вступили в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="61e6f-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="61e6f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="61e6f-121">See also</span></span>



[<span data-ttu-id="61e6f-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="61e6f-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

