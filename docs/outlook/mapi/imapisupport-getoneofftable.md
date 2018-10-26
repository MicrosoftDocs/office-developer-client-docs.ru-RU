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
ms.openlocfilehash: d54487928abcc889441ec9bf89ab6a10e5290062
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570837"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="a3a36-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="a3a36-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="a3a36-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3a36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3a36-105">Возвращает указатель на таблице одноразовых MAPI (список шаблонов, что все в адресной книге поставщиков поддержка создания новых получателей).</span><span class="sxs-lookup"><span data-stu-id="a3a36-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a3a36-106">���������</span><span class="sxs-lookup"><span data-stu-id="a3a36-106">Parameters</span></span>

 <span data-ttu-id="a3a36-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a3a36-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a3a36-108">[in] Битовая маска флаги, определяющее тип string столбцов.</span><span class="sxs-lookup"><span data-stu-id="a3a36-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="a3a36-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a3a36-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a3a36-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a3a36-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a3a36-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="a3a36-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="a3a36-112">Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a3a36-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="a3a36-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a3a36-113">_lppTable_</span></span>
  
> <span data-ttu-id="a3a36-114">[out] Указатель на указатель на одноразовых таблицы.</span><span class="sxs-lookup"><span data-stu-id="a3a36-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a3a36-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3a36-115">Return value</span></span>

<span data-ttu-id="a3a36-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3a36-116">S_OK</span></span> 
  
> <span data-ttu-id="a3a36-117">В таблице одноразовых был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="a3a36-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3a36-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="a3a36-118">Remarks</span></span>

<span data-ttu-id="a3a36-119">Метод **IMAPISupport::GetOneOffTable** реализуется для объектов поддержки поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a3a36-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="a3a36-120">Поставщиками адресной книги вызовите **GetOneOffTable** , чтобы получить полный список шаблонов для создания новых получателей.</span><span class="sxs-lookup"><span data-stu-id="a3a36-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="a3a36-121">В этой таблице включает в себя шаблоны, которые поддерживают поставщиками адресных книг, которые включены в сеансе, а также шаблоны, которые поддерживает MAPI.</span><span class="sxs-lookup"><span data-stu-id="a3a36-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="a3a36-122">Только что созданный получателей можно использовать адрес сообщения или можно добавить в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a3a36-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="a3a36-123">Список свойств, которые составляют обязательный столбец, задайте в одноразовых таблицах см в [Одноразовых таблиц](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a3a36-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="a3a36-124">Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a36-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a3a36-125">Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="a3a36-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a3a36-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a3a36-126">Notes to callers</span></span>

<span data-ttu-id="a3a36-127">Зарегистрированные для получения уведомлений об изменениях в этой таблице одноразовых также получат оповещений об изменениях в одноразовых таблицы других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="a3a36-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="a3a36-128">На основе этих уведомлений, может поддерживать новые типы адресов, которые добавляются во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="a3a36-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3a36-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a3a36-129">See also</span></span>



[<span data-ttu-id="a3a36-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="a3a36-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="a3a36-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="a3a36-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="a3a36-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3a36-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a3a36-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a3a36-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a3a36-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a3a36-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a3a36-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a3a36-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a3a36-136">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="a3a36-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="a3a36-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3a36-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="a3a36-138">Одноразовых таблиц</span><span class="sxs-lookup"><span data-stu-id="a3a36-138">One-Off Tables</span></span>](one-off-tables.md)

