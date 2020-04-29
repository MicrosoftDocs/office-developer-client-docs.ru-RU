---
title: иаблогонжетонеоффтабле
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
ms.openlocfilehash: 326a78ed512ec82a9f16b1540aad60954ab2d864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411878"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="f517e-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f517e-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="f517e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f517e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f517e-105">Возвращает таблицу из одноразовых шаблонов для создания получателей, добавляемых в список получателей исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f517e-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f517e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f517e-106">Parameters</span></span>

 <span data-ttu-id="f517e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f517e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f517e-108">возврата Битовая маска флагов, определяющих тип строковых столбцов, включенных в таблицу.</span><span class="sxs-lookup"><span data-stu-id="f517e-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="f517e-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f517e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f517e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f517e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f517e-111">Строковые столбцы представлены в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f517e-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f517e-112">Если флаг MAPI_UNICODE не установлен, строковые столбцы имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="f517e-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="f517e-113">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="f517e-113">_lppTable_</span></span>
  
> <span data-ttu-id="f517e-114">вышли Указатель на указатель на одноразовую таблицу.</span><span class="sxs-lookup"><span data-stu-id="f517e-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f517e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f517e-115">Return value</span></span>

<span data-ttu-id="f517e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f517e-116">S_OK</span></span> 
  
> <span data-ttu-id="f517e-117">Таблица с одноразовым извлечением успешно получена.</span><span class="sxs-lookup"><span data-stu-id="f517e-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="f517e-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f517e-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f517e-119">Установлен флаг MAPI_UNICODE, а поставщик адресных книг не поддерживает Юникод или MAPI_UNICODE не задан, а поставщик адресных книг поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f517e-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="f517e-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f517e-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f517e-121">Поставщик адресных книг не предоставляет одноразовых шаблонов.</span><span class="sxs-lookup"><span data-stu-id="f517e-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f517e-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="f517e-122">Remarks</span></span>

<span data-ttu-id="f517e-123">MAPI вызывает метод **жетонеоффтабле** , чтобы сделать доступными одноразовые шаблоны для создания получателей.</span><span class="sxs-lookup"><span data-stu-id="f517e-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="f517e-124">Новые получатели добавляются в список получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="f517e-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="f517e-125">Поставщики адресных книг должны поддерживать уведомления из одноразовой таблицы для информирования MAPI об изменениях шаблонов.</span><span class="sxs-lookup"><span data-stu-id="f517e-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="f517e-126">Для включения динамического обновления MAPI поддерживает односторонние таблицы Open.</span><span class="sxs-lookup"><span data-stu-id="f517e-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="f517e-127">Поставщики адресных книг также могут поддерживать одноразовую таблицу для каждого из их контейнеров.</span><span class="sxs-lookup"><span data-stu-id="f517e-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="f517e-128">Вызывающие объекты получают эту одноразовую таблицу, вызывая метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и запрашивает свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f517e-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="f517e-129">Шаблоны, доступные в этой таблице, используются для добавления получателей в контейнер.</span><span class="sxs-lookup"><span data-stu-id="f517e-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="f517e-130">Сведения о различиях между двумя типами одноразовых таблиц приведены в статье [Реализация одноразовых таблиц](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f517e-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="f517e-131">Список обязательных столбцов в одноразовой таблице поставщика адресных книг представлен в разделе [одноразовые таблицы](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f517e-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f517e-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f517e-132">See also</span></span>



[<span data-ttu-id="f517e-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f517e-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="f517e-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="f517e-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="f517e-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="f517e-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="f517e-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f517e-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

