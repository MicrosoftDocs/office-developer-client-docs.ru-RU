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
ms.openlocfilehash: 51a83e1e28534cc237419d9c4ae475c1d719c5de
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565076"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="f6344-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6344-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="f6344-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6344-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6344-105">Поддерживает доступ к объектам в таблице Microsoft Exchange Server, в частности доступа к системе управления список управления ДОСТУПОМ в таблице объекты и правила в таблице объекты на папок Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f6344-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="f6344-106">Имеет следующий вид: этот интерфейс [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса, но он обеспечивает поддержку структуры специфичных для сервера Microsoft Exchange, которые используются для управления доступом и правила.</span><span class="sxs-lookup"><span data-stu-id="f6344-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6344-107">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="f6344-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="f6344-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="f6344-108">None</span></span>  <br/> |
|<span data-ttu-id="f6344-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f6344-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="f6344-110">В таблице объекты сервера</span><span class="sxs-lookup"><span data-stu-id="f6344-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="f6344-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f6344-111">Called by:</span></span>  <br/> |<span data-ttu-id="f6344-112">MAPI и клиентских приложениях</span><span class="sxs-lookup"><span data-stu-id="f6344-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="f6344-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f6344-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f6344-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="f6344-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="f6344-115">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="f6344-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="f6344-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="f6344-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="f6344-117">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="f6344-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="f6344-118">В транзакции</span><span class="sxs-lookup"><span data-stu-id="f6344-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f6344-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="f6344-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f6344-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="f6344-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="f6344-121">Возвращает сведения о, последнюю ошибку в объекте таблицы.</span><span class="sxs-lookup"><span data-stu-id="f6344-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="f6344-122">Соответствие доступному</span><span class="sxs-lookup"><span data-stu-id="f6344-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="f6344-123">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6344-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="f6344-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="f6344-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="f6344-125">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6344-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="f6344-126">**Свойства, используемые для изменения таблицы правил**</span><span class="sxs-lookup"><span data-stu-id="f6344-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="f6344-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="f6344-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6344-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="f6344-148">**Свойства, используемые для изменения таблицы системный список управления ДОСТУПОМ**</span><span class="sxs-lookup"><span data-stu-id="f6344-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="f6344-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="f6344-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6344-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="f6344-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6344-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6344-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6344-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6344-158">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6344-158">Remarks</span></span>

<span data-ttu-id="f6344-159">Чтобы получить интерфейс **IExchangeModifyTable** , вызовите метод MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на свойство типа PT_OBJECT на объект folder.</span><span class="sxs-lookup"><span data-stu-id="f6344-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="f6344-160">При вызове метода **OpenProperty** передайте значение **IID_IExchangeModifyTable** с помощью параметра _lpiid_ .</span><span class="sxs-lookup"><span data-stu-id="f6344-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6344-161">См. также</span><span class="sxs-lookup"><span data-stu-id="f6344-161">See also</span></span>



[<span data-ttu-id="f6344-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="f6344-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

