---
title: Краткосрочные идентификаторы записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439564"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="15c33-103">Краткосрочные идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="15c33-103">Short-term entry identifiers</span></span>

<span data-ttu-id="15c33-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15c33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15c33-105">Краткосрочный идентификатор записи, присвоенный поставщиком услуг объекту, когда он должен быть быстро сконструированы и не должен длиться со временем или расстоянием.</span><span class="sxs-lookup"><span data-stu-id="15c33-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="15c33-106">Уникальность краткосрочного идентификатора записи гарантируется только в течение срока действия текущего сеанса на текущей рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="15c33-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="15c33-107">Обычно краткосрочный идентификатор записи действителен только до тех пор, пока объект, который он представляет, не будет отпущен.</span><span class="sxs-lookup"><span data-stu-id="15c33-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="15c33-108">Краткосрочные идентификаторы записей назначены строкам в таблицах и записям в диалоговых окнах, где необходимо быстро предоставить данные для просмотра.</span><span class="sxs-lookup"><span data-stu-id="15c33-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="15c33-109">Например, поставщики содержимого назначают краткосрочные идентификаторы записей строкам сообщений в таблице содержимого и получателям в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="15c33-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="15c33-110">Клиенты могут использовать эти краткосрочные идентификаторы записей для открытия объектов, представленных строками таблицы.</span><span class="sxs-lookup"><span data-stu-id="15c33-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="15c33-111">Однако в отличие от долгосрочных идентификаторов записей, которые можно использовать с любым из методов **OpenEntry,** краткосрочные идентификаторы записей следует использовать с методом **OpenEntry контейнера.**</span><span class="sxs-lookup"><span data-stu-id="15c33-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="15c33-112">Реализация краткосрочных идентификаторов записей</span><span class="sxs-lookup"><span data-stu-id="15c33-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="15c33-113">Наиболее распространенные способы реализации краткосрочных идентификаторов записей:</span><span class="sxs-lookup"><span data-stu-id="15c33-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="15c33-114">Делая краткосрочные идентификаторы записей тем же, что и долгосрочные идентификаторы, оставив все флаги не замеченными.</span><span class="sxs-lookup"><span data-stu-id="15c33-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="15c33-115">Делает краткосрочные идентификаторы записей не так, как долгосрочные идентификаторы, устанавливая все флаги.</span><span class="sxs-lookup"><span data-stu-id="15c33-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="15c33-116">Клиенты могут определить краткосрочный идентификатор записи второго типа, изучив его **член abFlags** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="15c33-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="15c33-117">Некоторые поставщики услуг очищают один или несколько флагов, чтобы создать краткосрочные идентификаторы записей, которые имеют большую ценность.</span><span class="sxs-lookup"><span data-stu-id="15c33-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="15c33-118">Например, следующие члены **abFlags** представляют краткосрочные идентификаторы записей, которые можно использовать в течение нескольких дней или для нескольких сеансов:</span><span class="sxs-lookup"><span data-stu-id="15c33-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="15c33-119">Клиенты быстро приобретают, используют и удаляют краткосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="15c33-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="15c33-120">По большей части их можно использовать так же, как и долгосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="15c33-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="15c33-121">Их можно извлечь из таблицы, передать в метод **OpenEntry** и сравнить с методом **CompareEntryIDs.**</span><span class="sxs-lookup"><span data-stu-id="15c33-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="15c33-122">Исключением является то, что они никогда не возвращаются из метода [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="15c33-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="15c33-123">Свойства, возвращаемые **getProps,** всегда являются долгосрочными идентификаторами записей.</span><span class="sxs-lookup"><span data-stu-id="15c33-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15c33-124">См. также</span><span class="sxs-lookup"><span data-stu-id="15c33-124">See also</span></span>

- [<span data-ttu-id="15c33-125">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="15c33-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

