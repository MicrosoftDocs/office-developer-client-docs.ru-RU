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
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812288"
---
# <a name="short-term-entry-identifiers"></a><span data-ttu-id="bdc4d-103">Краткосрочные идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="bdc4d-103">Short-term entry identifiers</span></span>

<span data-ttu-id="bdc4d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bdc4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bdc4d-105">Краткосрочные идентификатор записи назначается поставщиком услуг на объект при идентификатор должен быть быстро и не требуется последнего по времени или расстояние.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-105">A short-term entry identifier is assigned by a service provider to an object when the identifier must be constructed quickly and does not need to last over time or distance.</span></span> <span data-ttu-id="bdc4d-106">Уникальность краткосрочных идентификатор записи гарантируется только в течение текущего сеанса на текущей рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-106">The uniqueness of a short-term entry identifier is guaranteed only over the life of the current session on the current workstation.</span></span> <span data-ttu-id="bdc4d-107">Как правило краткосрочных идентификатор записи действителен только в том случае, пока выпущен представляющий его объект.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-107">Typically, a short-term entry identifier is valid only until the object that it represents is released.</span></span> 
  
<span data-ttu-id="bdc4d-108">Краткосрочные идентификаторы записей назначаются для строк в таблицах и записей в диалоговых окнах, где это необходимо для предоставления данных быстро для просмотра.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-108">Short-term entry identifiers are assigned to rows in tables and to entries in dialog boxes, where it is necessary to provide data quickly for browsing.</span></span> <span data-ttu-id="bdc4d-109">Например поставщиков хранилища сообщений назначение краткосрочных идентификаторы записей строкам сообщений в таблице содержимое и список получателей в таблице получателей.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-109">For example, message store providers assign short-term entry identifiers to rows of messages in a contents table and to recipients in a recipients table.</span></span> 

<span data-ttu-id="bdc4d-110">Клиенты могут использовать эти краткосрочных идентификаторы записей для открытия объектов, представленных в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-110">Clients can use these short-term entry identifiers to open the objects represented by the table rows.</span></span> <span data-ttu-id="bdc4d-111">Тем не менее в отличие от долгосрочного идентификаторы записей, которые можно использовать с любой из способов **OpenEntry** , краткосрочных идентификаторы записей можно использовать с методом **OpenEntry** контейнера.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-111">However, unlike long-term entry identifiers that can be used with any of the **OpenEntry** methods, short-term entry identifiers should be used with the container's **OpenEntry** method.</span></span> 
  
## <a name="implementing-short-term-entry-identifiers"></a><span data-ttu-id="bdc4d-112">Реализация краткосрочных идентификаторы записей</span><span class="sxs-lookup"><span data-stu-id="bdc4d-112">Implementing short-term entry identifiers</span></span>

<span data-ttu-id="bdc4d-113">Наиболее распространенные способы реализации краткосрочных идентификаторы записей относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="bdc4d-113">The most common ways to implement short-term entry identifiers include the following:</span></span>
  
- <span data-ttu-id="bdc4d-114">То же, что долгосрочного идентификаторы, сохраняя все флаги неопределенные внесения краткосрочных идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-114">Making the short-term entry identifiers the same as the long-term identifiers, leaving all of the flags unset.</span></span> 
    
- <span data-ttu-id="bdc4d-115">Отображение краткосрочных идентификаторы записей отличается от долгосрочного, параметр все флаги идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-115">Making the short-term entry identifiers different from the long-term identifiers, setting all of the flags.</span></span> 
    
<span data-ttu-id="bdc4d-116">Клиенты могут определять краткосрочных идентификатор записи второго типа, проверив его элементом **abFlags** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bdc4d-116">Clients can identify a short-term entry identifier of the second type by examining its **abFlags** member as follows:</span></span> 
  
```cpp
abFlags[0] = 0xFF;
 
```

<span data-ttu-id="bdc4d-117">Некоторые поставщики услуг снимите один или несколько флагов для создания краткосрочных идентификаторы записей, имеющих более действия.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-117">Some service providers clear one or more flags to create short-term entry identifiers that have greater validity.</span></span> <span data-ttu-id="bdc4d-118">Например следующие члены **abFlags** представляют краткосрочных идентификаторы записей, которые могут использоваться для нескольких дней или для нескольких сеансов:</span><span class="sxs-lookup"><span data-stu-id="bdc4d-118">For example, the following **abFlags** members represent short-term entry identifiers that can be used for multiple days or for multiple sessions:</span></span> 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

<span data-ttu-id="bdc4d-119">Клиенты быстро получить, использование и отменить краткосрочных идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-119">Clients quickly acquire, use, and discard short-term entry identifiers.</span></span> <span data-ttu-id="bdc4d-120">В большинстве случаев их можно использовать в так же, как долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-120">For the most part, they can be used in the same manner as long-term entry identifiers.</span></span> <span data-ttu-id="bdc4d-121">Они могут быть получены из таблицы, переданной в метод **OpenEntry** и по сравнению с помощью метода **CompareEntryIDs** .</span><span class="sxs-lookup"><span data-stu-id="bdc4d-121">They can be retrieved from a table, passed to the **OpenEntry** method, and compared with the **CompareEntryIDs** method.</span></span> <span data-ttu-id="bdc4d-122">Одно исключение — они никогда не возврат из метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="bdc4d-122">The one exception is that they are never returned from the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="bdc4d-123">Свойства, возвращенные **GetProps** всегда являются долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="bdc4d-123">The properties returned from **GetProps** are always long-term entry identifiers.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bdc4d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="bdc4d-124">See also</span></span>

- [<span data-ttu-id="bdc4d-125">Идентификаторы MAPI записей</span><span class="sxs-lookup"><span data-stu-id="bdc4d-125">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

