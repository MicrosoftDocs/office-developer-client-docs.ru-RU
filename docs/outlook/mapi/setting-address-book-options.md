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
# <a name="setting-address-book-options"></a><span data-ttu-id="4cc92-103">Настройка параметров адресной книги</span><span class="sxs-lookup"><span data-stu-id="4cc92-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="4cc92-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cc92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cc92-105">Вы можете задать три свойства, описывающих параметры использования адресной книги:</span><span class="sxs-lookup"><span data-stu-id="4cc92-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="4cc92-106">**Пр_аб_сеарч_пас** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cc92-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="4cc92-107">Свойство **пр_аб_сеарч_пас** используется [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка, в котором они должны быть задействованы.</span><span class="sxs-lookup"><span data-stu-id="4cc92-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="4cc92-108">Для каждого контейнера в **пр_аб_сеарч_пас**, **IAddrBook:: Ресолвенаме** вызывает метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc92-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="4cc92-109">Контейнеры в начале **пр_аб_сеарч_пас** ищутся перед контейнерами в конце **пр_аб_сеарч_пас**.</span><span class="sxs-lookup"><span data-stu-id="4cc92-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="4cc92-110">Порядок поиска в **пр_аб_сеарч_пас** указывается с помощью структуры [SRowSet](srowset.md) , той же структуры, которая используется для представления строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="4cc92-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="4cc92-111">Вы можете просмотреть текущий путь поиска, вызвав метод [IAddrBook:: жетсеарчпас](iaddrbook-getsearchpath.md) и изменив его, вызвав метод [IAddrBook:: сетсеарчпас](iaddrbook-setsearchpath.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc92-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="4cc92-112">**Пр_аб_дефаулт_дир** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cc92-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="4cc92-113">Свойство **пр_аб_дефаулт_дир** — это идентификатор записи контейнера адресной книги, который будет отображаться первоначально при отображении адресной книги.</span><span class="sxs-lookup"><span data-stu-id="4cc92-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="4cc92-114">Параметры каталога по умолчанию действуют до тех пор, пока вы не измените его, вызвав метод [IAddrBook:: сетдефаултдир](iaddrbook-setdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc92-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="4cc92-115">Вы можете просмотреть каталог по умолчанию, вызвав метод [IAddrBook:: жетдефаултдир](iaddrbook-getdefaultdir.md) .</span><span class="sxs-lookup"><span data-stu-id="4cc92-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="4cc92-116">**Пр_аб_дефаулт_паб** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4cc92-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="4cc92-117">Эти три свойства являются особыми, так как вы не можете работать с ними с помощью стандартных методов **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="4cc92-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="4cc92-118">Вместо этого необходимо использовать методы **IAddrBook** .</span><span class="sxs-lookup"><span data-stu-id="4cc92-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="4cc92-119">Так как ни одно из этих свойств не может быть изменено с помощью **IMAPIProp:: SetProps**, нет необходимости вызывать **IMAPIProp:: SaveChanges** , чтобы сделать изменения постоянными.</span><span class="sxs-lookup"><span data-stu-id="4cc92-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="4cc92-120">Изменения, внесенные с помощью методов **IAddrBook** , вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="4cc92-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4cc92-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4cc92-121">See also</span></span>



[<span data-ttu-id="4cc92-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4cc92-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

