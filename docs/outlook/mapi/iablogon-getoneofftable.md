---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3732d8cbfaf9a6a10c62eae9e7a12b04de8a80ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583682"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="2c064-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="2c064-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="2c064-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c064-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c064-105">Возвращает таблицу одноразовых шаблоны для создания получателей для добавления в список получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c064-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="2c064-106">���������</span><span class="sxs-lookup"><span data-stu-id="2c064-106">Parameters</span></span>

 <span data-ttu-id="2c064-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2c064-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2c064-108">[in] Битовая маска флаги, определяющее тип string столбцов, указанных в таблице.</span><span class="sxs-lookup"><span data-stu-id="2c064-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="2c064-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2c064-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2c064-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c064-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2c064-111">Столбцы строку, в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2c064-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="2c064-112">Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2c064-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="2c064-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="2c064-113">_lppTable_</span></span>
  
> <span data-ttu-id="2c064-114">[out] Указатель на указатель на одноразовых таблицы.</span><span class="sxs-lookup"><span data-stu-id="2c064-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2c064-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c064-115">Return value</span></span>

<span data-ttu-id="2c064-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="2c064-116">S_OK</span></span> 
  
> <span data-ttu-id="2c064-117">В таблице одноразовых был успешно извлечен.</span><span class="sxs-lookup"><span data-stu-id="2c064-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="2c064-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2c064-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2c064-119">Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="2c064-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="2c064-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="2c064-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="2c064-121">Поставщик адресной книги не предоставляет никаких одноразовых шаблонов.</span><span class="sxs-lookup"><span data-stu-id="2c064-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2c064-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="2c064-122">Remarks</span></span>

<span data-ttu-id="2c064-123">MAPI вызывает метод **GetOneOffTable** , чтобы сделать доступных одноразовых шаблонов для создания получателей.</span><span class="sxs-lookup"><span data-stu-id="2c064-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="2c064-124">Новые получатели добавляются в список получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="2c064-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="2c064-125">Поставщиками адресных книг должны поддерживать уведомлений на их одноразовых таблицу, чтобы информировать MAPI изменения шаблона.</span><span class="sxs-lookup"><span data-stu-id="2c064-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="2c064-126">MAPI отслеживает одноразовых таблицы, открыть, чтобы включить динамическое обновление.</span><span class="sxs-lookup"><span data-stu-id="2c064-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="2c064-127">Поставщиками адресной книги также могут поддерживать одноразовых таблице для каждого из их контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2c064-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="2c064-128">Вызывающие извлечение одноразовых таблице путем вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера и разрешения на запрос свойства **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2c064-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="2c064-129">Шаблоны, доступные через этой таблице используются для добавления получателей в контейнере.</span><span class="sxs-lookup"><span data-stu-id="2c064-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="2c064-130">Обсуждение различия между двумя типами одноразовых таблиц [Реализация одноразовых таблиц](implementing-one-off-tables.md)см.</span><span class="sxs-lookup"><span data-stu-id="2c064-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="2c064-131">Список обязательные столбцы в таблице одноразовых поставщика адресных книг см в [Одноразовых таблиц](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2c064-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c064-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2c064-132">See also</span></span>



[<span data-ttu-id="2c064-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="2c064-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="2c064-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="2c064-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="2c064-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="2c064-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="2c064-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2c064-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

