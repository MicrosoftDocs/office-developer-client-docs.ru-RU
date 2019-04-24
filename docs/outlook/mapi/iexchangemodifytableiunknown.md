---
title: Иексчанжемодифитабле IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable
api_type:
- COM
ms.assetid: 45a73c7b-5855-4b70-866b-facb41cb3c32
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350885"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="cec0d-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cec0d-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="cec0d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cec0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cec0d-105">Поддерживает доступ к объектам таблицы Microsoft Exchange Server, а именно к объектам таблицы и объектам таблицы правил списка управления доступом в папках Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="cec0d-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="cec0d-106">Этот интерфейс напоминает интерфейс [IMAPITable: IUnknown](imapitableiunknown.md) , но он добавляет поддержку для отдельных структур Microsoft Exchange Server, которые используются для управления таблицами управления доступом и правилами.</span><span class="sxs-lookup"><span data-stu-id="cec0d-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cec0d-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="cec0d-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="cec0d-108">Нет</span><span class="sxs-lookup"><span data-stu-id="cec0d-108">None</span></span>  <br/> |
|<span data-ttu-id="cec0d-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cec0d-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="cec0d-110">Объекты таблицы сервера</span><span class="sxs-lookup"><span data-stu-id="cec0d-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="cec0d-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cec0d-111">Called by:</span></span>  <br/> |<span data-ttu-id="cec0d-112">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="cec0d-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="cec0d-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="cec0d-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cec0d-114">Иид_иексчанжемодифитабле</span><span class="sxs-lookup"><span data-stu-id="cec0d-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="cec0d-115">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="cec0d-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="cec0d-116">ЛПЕКСЧАНЖЕМОДИФИТАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="cec0d-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="cec0d-117">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="cec0d-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="cec0d-118">Транзакции</span><span class="sxs-lookup"><span data-stu-id="cec0d-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cec0d-119">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="cec0d-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cec0d-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="cec0d-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="cec0d-121">Возвращает сведения о последней ошибке, произошедшей в объекте Table.</span><span class="sxs-lookup"><span data-stu-id="cec0d-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="cec0d-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="cec0d-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="cec0d-123">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="cec0d-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="cec0d-124">Модифитабле</span><span class="sxs-lookup"><span data-stu-id="cec0d-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="cec0d-125">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="cec0d-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="cec0d-126">**Свойства, используемые для изменения таблицы Rules**</span><span class="sxs-lookup"><span data-stu-id="cec0d-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="cec0d-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="cec0d-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cec0d-128">**Пр_руле_актионс** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-130">**Пр_руле_кондитион** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-132">**Пр_руле_ид** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-134">**Пр_руле_левел** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-136">**Пр_руле_наме** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-138">**Пр_руле_провидер** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-140">**Пр_руле_провидер_дата** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-142">**Пр_руле_секуенце** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-144">**Пр_руле_стате** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-146">**Пр_руле_усер_флагс** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="cec0d-148">**Свойства, используемые для изменения таблицы SACL**</span><span class="sxs-lookup"><span data-stu-id="cec0d-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="cec0d-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="cec0d-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cec0d-150">**Пр_мембер_ентрид** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-152">**Пр_мембер_ид** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-154">**Пр_мембер_наме** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="cec0d-156">**Пр_мембер_ригхтс** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cec0d-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cec0d-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="cec0d-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cec0d-158">Примечания</span><span class="sxs-lookup"><span data-stu-id="cec0d-158">Remarks</span></span>

<span data-ttu-id="cec0d-159">Чтобы получить интерфейс **иексчанжемодифитабле** , вызовите метод MAPI [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для свойства типа пт_обжект объекта Folder.</span><span class="sxs-lookup"><span data-stu-id="cec0d-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="cec0d-160">При вызове метода **опенпроперти** передайте значение **иид_иексчанжемодифитабле** в параметре _лпиид_ .</span><span class="sxs-lookup"><span data-stu-id="cec0d-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cec0d-161">См. также</span><span class="sxs-lookup"><span data-stu-id="cec0d-161">See also</span></span>



[<span data-ttu-id="cec0d-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="cec0d-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

