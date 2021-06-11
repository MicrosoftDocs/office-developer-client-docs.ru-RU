---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412760"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="a734c-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="a734c-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="a734c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a734c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a734c-105">Возвращает указатель в разовую таблицу MAPI (список шаблонов, которые все поставщики адресных книг поддерживают для создания новых получателей).</span><span class="sxs-lookup"><span data-stu-id="a734c-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a734c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a734c-106">Parameters</span></span>

 <span data-ttu-id="a734c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a734c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a734c-108">[in] Битмашка флагов, контролируемая типом столбцов строки.</span><span class="sxs-lookup"><span data-stu-id="a734c-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="a734c-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a734c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a734c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a734c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a734c-111">Столбцы строк находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="a734c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="a734c-112">Если флаг MAPI_UNICODE не установлен, столбцы строк находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a734c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="a734c-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a734c-113">_lppTable_</span></span>
  
> <span data-ttu-id="a734c-114">[вышел] Указатель на указатель на разовую таблицу.</span><span class="sxs-lookup"><span data-stu-id="a734c-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a734c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a734c-115">Return value</span></span>

<span data-ttu-id="a734c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a734c-116">S_OK</span></span> 
  
> <span data-ttu-id="a734c-117">Разовая таблица была успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="a734c-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a734c-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="a734c-118">Remarks</span></span>

<span data-ttu-id="a734c-119">Метод **IMAPISupport::GetOneOffTable** реализован для объектов поддержки поставщиков адресных книг.</span><span class="sxs-lookup"><span data-stu-id="a734c-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="a734c-120">Поставщики адресных книг звонят **в GetOneOffTable,** чтобы получить полный список шаблонов для создания новых получателей.</span><span class="sxs-lookup"><span data-stu-id="a734c-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="a734c-121">В эту таблицу включены шаблоны, которые поддерживают поставщики адресных книг, которые активно поддерживают сеанс, а также шаблоны, поддерживаемые MAPI.</span><span class="sxs-lookup"><span data-stu-id="a734c-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="a734c-122">Вновь созданные получатели могут использоваться для обращения к сообщению или могут быть добавлены в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a734c-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="a734c-123">Список свойств, которые составляют необходимый столбец, установленный в разовых таблицах, см. в статье [One-Off Tables.](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="a734c-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="a734c-124">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="a734c-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a734c-125">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="a734c-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a734c-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a734c-126">Notes to callers</span></span>

<span data-ttu-id="a734c-127">Если вы зарегистрированы для получения уведомлений об изменениях в этой разовой таблице, вы также будете получать уведомления об изменениях в разовых таблицах других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a734c-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="a734c-128">На основе этих уведомлений можно поддерживать новые типы адресов, добавленные во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="a734c-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a734c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a734c-129">See also</span></span>



[<span data-ttu-id="a734c-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="a734c-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="a734c-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="a734c-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="a734c-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a734c-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a734c-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a734c-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a734c-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a734c-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a734c-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a734c-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a734c-136">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="a734c-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="a734c-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a734c-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="a734c-138">Разовые таблицы</span><span class="sxs-lookup"><span data-stu-id="a734c-138">One-Off Tables</span></span>](one-off-tables.md)

