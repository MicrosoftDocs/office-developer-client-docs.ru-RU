---
title: Имаписуппортжетонеоффтабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316578"
---
# <a name="imapisupportgetoneofftable"></a><span data-ttu-id="1de8b-103">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="1de8b-103">IMAPISupport::GetOneOffTable</span></span>

  
  
<span data-ttu-id="1de8b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1de8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1de8b-105">Возвращает указатель на одноразовую таблицу MAPI (список шаблонов, которые поддерживаются всеми поставщиками адресных книг для создания новых получателей).</span><span class="sxs-lookup"><span data-stu-id="1de8b-105">Returns a pointer to the MAPI one-off table (a list of templates that all address book providers support for creating new recipients).</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="1de8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1de8b-106">Parameters</span></span>

 <span data-ttu-id="1de8b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1de8b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1de8b-108">возврата Битовая маска флагов, определяющих тип строковых столбцов.</span><span class="sxs-lookup"><span data-stu-id="1de8b-108">[in] A bitmask of flags that controls the type of the string columns.</span></span> <span data-ttu-id="1de8b-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1de8b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="1de8b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1de8b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1de8b-111">Строковые столбцы представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="1de8b-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="1de8b-112">Если флаг МАПИ_УНИКОДЕ не установлен, строковые столбцы представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1de8b-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="1de8b-113">_Лпптабле_</span><span class="sxs-lookup"><span data-stu-id="1de8b-113">_lppTable_</span></span>
  
> <span data-ttu-id="1de8b-114">вышли Указатель на указатель на одноразовую таблицу.</span><span class="sxs-lookup"><span data-stu-id="1de8b-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1de8b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1de8b-115">Return value</span></span>

<span data-ttu-id="1de8b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1de8b-116">S_OK</span></span> 
  
> <span data-ttu-id="1de8b-117">Таблица с одноразовым извлечением успешно получена.</span><span class="sxs-lookup"><span data-stu-id="1de8b-117">The one-off table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1de8b-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="1de8b-118">Remarks</span></span>

<span data-ttu-id="1de8b-119">Метод **имаписуппорт:: жетонеоффтабле** реализован для объектов поддержки поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="1de8b-119">The **IMAPISupport::GetOneOffTable** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="1de8b-120">Поставщики адресных книг вызывают **жетонеоффтабле** , чтобы получить полный список шаблонов для создания новых получателей.</span><span class="sxs-lookup"><span data-stu-id="1de8b-120">Address book providers call **GetOneOffTable** to retrieve the complete list of templates for creating new recipients.</span></span> <span data-ttu-id="1de8b-121">В этой таблице содержатся шаблоны, которые поддерживаются активными поставщиками книг, которые активны во время сеанса, а также шаблоны, поддерживаемые MAPI.</span><span class="sxs-lookup"><span data-stu-id="1de8b-121">This table includes templates that address book providers that are active in the session support, as well as templates that MAPI supports.</span></span> 
  
<span data-ttu-id="1de8b-122">Только что созданные получатели могут быть использованы для обращения к сообщению или могут быть добавлены в контейнер адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1de8b-122">The newly created recipients can be used to address a message or can be added to an address book container.</span></span>
  
<span data-ttu-id="1de8b-123">Список свойств, составляющих обязательный набор столбцов в одноразовых таблицах, приведен в разделе [одноразовЫе таблицы](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1de8b-123">For a list of the properties that make up the required column set in one-off tables, see [One-Off Tables](one-off-tables.md).</span></span>
  
<span data-ttu-id="1de8b-124">Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="1de8b-124">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="1de8b-125">Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="1de8b-125">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1de8b-126">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1de8b-126">Notes to callers</span></span>

<span data-ttu-id="1de8b-127">Если вы зарегистрированы, чтобы получать уведомления об изменениях, внесенных в эту одноразовую таблицу, вы также получите уведомления об изменениях в одноразовых таблицах поставщиков.</span><span class="sxs-lookup"><span data-stu-id="1de8b-127">If you are registered to receive notifications of changes to this one-off table, you will also receive notifications of changes to other providers' one-off tables.</span></span> <span data-ttu-id="1de8b-128">На основе этих уведомлений вы можете поддерживать новые типы адресов, добавленные во время текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="1de8b-128">Based on these notifications, you can support new address types that are added during the current session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1de8b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1de8b-129">See also</span></span>



[<span data-ttu-id="1de8b-130">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="1de8b-130">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="1de8b-131">IMAPISupport::NewEntry</span><span class="sxs-lookup"><span data-stu-id="1de8b-131">IMAPISupport::NewEntry</span></span>](imapisupport-newentry.md)
  
[<span data-ttu-id="1de8b-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1de8b-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="1de8b-133">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="1de8b-133">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="1de8b-134">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1de8b-134">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="1de8b-135">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="1de8b-135">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="1de8b-136">Каноническое свойство PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="1de8b-136">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="1de8b-137">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1de8b-137">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="1de8b-138">Одноразовые таблицы</span><span class="sxs-lookup"><span data-stu-id="1de8b-138">One-Off Tables</span></span>](one-off-tables.md)

