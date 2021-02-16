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
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="b1461-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="b1461-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="b1461-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1461-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1461-105">Возвращает указатель на односервную таблицу MAPI (список шаблонов, поддерживаемый всеми поставщиками адресных книг для создания новых получателей).</span><span class="sxs-lookup"><span data-stu-id="b1461-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="b1461-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1461-106">Parameters</span></span>

 <span data-ttu-id="b1461-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1461-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b1461-108">[in] Битоваяmas флагов, которая управляет типом строки столбцов.</span><span class="sxs-lookup"><span data-stu-id="b1461-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="b1461-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b1461-109">The following flag can be set:</span></span>
    
<span data-ttu-id="b1461-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b1461-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b1461-111">Строки столбцов в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b1461-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="b1461-112">Если флаг MAPI_UNICODE не установлен, строки столбцов имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1461-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="b1461-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b1461-113">_lppTable_</span></span>
  
> <span data-ttu-id="b1461-114">[out] Указатель на указатель на одностолевую таблицу.</span><span class="sxs-lookup"><span data-stu-id="b1461-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b1461-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1461-115">Return value</span></span>

<span data-ttu-id="b1461-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b1461-116">S_OK</span></span> 
  
> <span data-ttu-id="b1461-117">Односеаленная таблица была успешно извлечена.</span><span class="sxs-lookup"><span data-stu-id="b1461-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b1461-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1461-118">Remarks</span></span>

<span data-ttu-id="b1461-119">Метод **IMAPISupport::GetOneOffTable реализован** для объектов поддержки поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b1461-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="b1461-120">Поставщики адресных книг **звонят в GetOneOffTable,** чтобы получить полный список шаблонов для создания новых получателей.</span><span class="sxs-lookup"><span data-stu-id="b1461-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="b1461-121">В эту таблицу входят шаблоны, которые включают поставщиков адресных книг, активных в поддержке сеанса, а также шаблоны, поддерживаемые MAPI.</span><span class="sxs-lookup"><span data-stu-id="b1461-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="b1461-122">Созданные получатели можно использовать для обращения к сообщению или добавить в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b1461-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="b1461-123">Список свойств, которые составляют необходимый столбец, задав в однонастройных таблицах, см. в статье ["Разовые таблицы".](one-off-tables.md)</span><span class="sxs-lookup"><span data-stu-id="b1461-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="b1461-124">Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="b1461-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="b1461-125">Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="b1461-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b1461-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b1461-126">Notes to callers</span></span>

<span data-ttu-id="b1461-127">Если вы зарегистрированы для получения уведомлений об изменениях в этой разной таблице, вы также будете получать уведомления об изменениях в разовых таблицах других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="b1461-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="b1461-128">На основе этих уведомлений можно поддерживать новые типы адресов, добавленные во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="b1461-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1461-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b1461-129">See also</span></span>



[<span data-ttu-id="b1461-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="b1461-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="b1461-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="b1461-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="b1461-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1461-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="b1461-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="b1461-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="b1461-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="b1461-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="b1461-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="b1461-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="b1461-136">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="b1461-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="b1461-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1461-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="b1461-138">Разовые таблицы</span><span class="sxs-lookup"><span data-stu-id="b1461-138">One-Off Tables</span></span>](one-off-tables.md)

