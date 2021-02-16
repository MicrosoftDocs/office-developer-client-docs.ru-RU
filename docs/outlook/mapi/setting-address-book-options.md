---
title: Настройка параметров адресной книги
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
# <a name="setting-address-book-options"></a><span data-ttu-id="4b6cd-103">Настройка параметров адресной книги</span><span class="sxs-lookup"><span data-stu-id="4b6cd-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="4b6cd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b6cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b6cd-105">Можно настроить три свойства, описывая параметры использования адресной книги:</span><span class="sxs-lookup"><span data-stu-id="4b6cd-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="4b6cd-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="4b6cd-107">Свойство **PR_AB_SEARCH_PATH** используется [IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка их использования.</span><span class="sxs-lookup"><span data-stu-id="4b6cd-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="4b6cd-108">Для каждого контейнера **в PR_AB_SEARCH_PATH** **IAddrBook::ResolveName** вызывает метод [IABContainer::ResolveNames.](iabcontainer-resolvenames.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="4b6cd-109">Контейнеры в начале **PR_AB_SEARCH_PATH** перед контейнерами в конце **PR_AB_SEARCH_PATH.**</span><span class="sxs-lookup"><span data-stu-id="4b6cd-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="4b6cd-110">Порядок поиска в **PR_AB_SEARCH_PATH** задан с помощью структуры [SRowSet,](srowset.md) той же структуры, которая используется для представления строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="4b6cd-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="4b6cd-111">Чтобы просмотреть текущий путь поиска, вы можете вызывать метод [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и изменять его, вызывая метод [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="4b6cd-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4b6cd-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="4b6cd-113">Свойство **PR_AB_DEFAULT_DIR** является идентификатором записи контейнера адресной книги, который будет отображаться изначально при отобраствии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4b6cd-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="4b6cd-114">Параметр каталога по умолчанию остается в силе, пока вы не измените его, вызывая метод [IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="4b6cd-115">Чтобы просмотреть каталог по умолчанию, вы можете вызывать метод [IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="4b6cd-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab)](pidtagabdefaultpab-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="4b6cd-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="4b6cd-117">Эти три свойства являются специальными, так как с ними невозможно работать с помощью стандартных методов **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="4b6cd-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="4b6cd-118">Вместо этого необходимо использовать методы **IAddrBook.**</span><span class="sxs-lookup"><span data-stu-id="4b6cd-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="4b6cd-119">Так как ни одно из этих свойств не может быть изменено с помощью **IMAPIProp::SetProps,** нет необходимости вызывать **IMAPIProp::SaveChanges,** чтобы внести изменения без изменений.</span><span class="sxs-lookup"><span data-stu-id="4b6cd-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="4b6cd-120">Изменения, внося в методы **IAddrBook, вступает** в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="4b6cd-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b6cd-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4b6cd-121">See also</span></span>



[<span data-ttu-id="4b6cd-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4b6cd-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

