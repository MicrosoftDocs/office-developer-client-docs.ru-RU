---
title: Параметры настройки адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417345"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="7f0bb-103">Параметры настройки адресной книги</span><span class="sxs-lookup"><span data-stu-id="7f0bb-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="7f0bb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f0bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f0bb-105">Можно установить три свойства, описывая варианты использования адресной книги:</span><span class="sxs-lookup"><span data-stu-id="7f0bb-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="7f0bb-106">**PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="7f0bb-107">Свойство **PR_AB_SEARCH_PATH** [используется IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка их участия.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="7f0bb-108">Для каждого контейнера **в PR_AB_SEARCH_PATH,** **IAddrBook::ResolveName** вызывает свой [метод IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="7f0bb-109">Контейнеры в начале **PR_AB_SEARCH_PATH** до контейнеров в конце **PR_AB_SEARCH_PATH**.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="7f0bb-110">Порядок поиска **в PR_AB_SEARCH_PATH** указывается с помощью структуры [SRowSet,](srowset.md) той же структуры, которая используется для представления строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="7f0bb-111">Вы можете просмотреть текущий путь поиска, позвонив [методу IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и измените его, назвав [метод IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="7f0bb-112">**PR_AB_DEFAULT_DIR** [(PidTagAbDefaultDir)](pidtagabdefaultdir-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="7f0bb-113">Свойство **PR_AB_DEFAULT_DIR** является идентификатором входа контейнера адресной книги, который будет отображаться на начальном этапе при отобраствии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="7f0bb-114">Параметр каталога по умолчанию остается в силе до тех пор, пока вы не измените его, назвав [метод IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="7f0bb-115">Вы можете просмотреть каталог по умолчанию, позвонив [методу IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="7f0bb-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="7f0bb-116">**PR_AB_DEFAULT_PAB** [(PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7f0bb-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="7f0bb-117">Эти три свойства являются особыми, так как с ними нельзя работать с помощью стандартных **методов IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="7f0bb-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="7f0bb-118">Вместо этого необходимо использовать **методы IAddrBook.**</span><span class="sxs-lookup"><span data-stu-id="7f0bb-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="7f0bb-119">Поскольку ни одно из этих свойств не может быть изменено с **помощью IMAPIProp::SetProps,** нет необходимости вызывать **IMAPIProp::SaveChanges,** чтобы внести изменения навсегда.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="7f0bb-120">Изменения, сделанные с помощью **методов IAddrBook,** вступает в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="7f0bb-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f0bb-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7f0bb-121">See also</span></span>



[<span data-ttu-id="7f0bb-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7f0bb-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

