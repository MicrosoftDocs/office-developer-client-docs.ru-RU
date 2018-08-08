---
title: IExchangeModifyTable IUnknown
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
ms.openlocfilehash: 1093975e6cbdd79004125a0a4a3098ffa421ab0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808808"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="76809-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76809-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="76809-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="76809-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="76809-105">Поддерживает доступ к объектам в таблице Microsoft Exchange Server, в частности доступа к системе управления список управления ДОСТУПОМ в таблице объекты и правила в таблице объекты на папок Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="76809-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="76809-106">Имеет следующий вид: этот интерфейс [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса, но он обеспечивает поддержку структуры специфичных для сервера Microsoft Exchange, которые используются для управления доступом и правила.</span><span class="sxs-lookup"><span data-stu-id="76809-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76809-107">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="76809-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="76809-108">Нет</span><span class="sxs-lookup"><span data-stu-id="76809-108">None</span></span>  <br/> |
|<span data-ttu-id="76809-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="76809-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="76809-110">В таблице объекты сервера</span><span class="sxs-lookup"><span data-stu-id="76809-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="76809-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="76809-111">Called by:</span></span>  <br/> |<span data-ttu-id="76809-112">MAPI и клиентских приложениях</span><span class="sxs-lookup"><span data-stu-id="76809-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="76809-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="76809-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76809-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="76809-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="76809-115">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="76809-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="76809-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="76809-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="76809-117">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="76809-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="76809-118">В транзакции</span><span class="sxs-lookup"><span data-stu-id="76809-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76809-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="76809-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76809-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="76809-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="76809-121">Возвращает сведения о, последнюю ошибку в объекте таблицы.</span><span class="sxs-lookup"><span data-stu-id="76809-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="76809-122">Соответствие доступному</span><span class="sxs-lookup"><span data-stu-id="76809-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="76809-123">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="76809-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="76809-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="76809-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="76809-125">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="76809-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="76809-126">**Свойства, используемые для изменения таблицы правил**</span><span class="sxs-lookup"><span data-stu-id="76809-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="76809-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="76809-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76809-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="76809-148">**Свойства, используемые для изменения таблицы системный список управления ДОСТУПОМ**</span><span class="sxs-lookup"><span data-stu-id="76809-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="76809-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="76809-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76809-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="76809-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="76809-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="76809-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="76809-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76809-158">Замечания</span><span class="sxs-lookup"><span data-stu-id="76809-158">Remarks</span></span>

<span data-ttu-id="76809-159">Чтобы получить интерфейс **IExchangeModifyTable** , вызовите метод MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на свойство типа PT_OBJECT на объект folder.</span><span class="sxs-lookup"><span data-stu-id="76809-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="76809-160">При вызове метода **OpenProperty** передайте значение **IID_IExchangeModifyTable** с помощью параметра _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="76809-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76809-161">См. также</span><span class="sxs-lookup"><span data-stu-id="76809-161">See also</span></span>



[<span data-ttu-id="76809-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="76809-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

