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
ms.openlocfilehash: 333e1d5cacc069ee1faef01426a1c0a60ef07f8e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418108"
---
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="24142-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24142-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="24142-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24142-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24142-105">Поддерживает доступ к объектам Microsoft Exchange Server таблиц, в частности объектам таблицы списка управления доступом системы (SACL) и объектам таблиц правил в Microsoft Exchange Server папок.</span><span class="sxs-lookup"><span data-stu-id="24142-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="24142-106">Этот интерфейс похож на интерфейс [IMAPITable : IUnknown,](imapitableiunknown.md) но он добавляет поддержку Microsoft Exchange Server структур, используемых для управления SACLs и правилами.</span><span class="sxs-lookup"><span data-stu-id="24142-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24142-107">Выставим:</span><span class="sxs-lookup"><span data-stu-id="24142-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="24142-108">Нет</span><span class="sxs-lookup"><span data-stu-id="24142-108">None</span></span>  <br/> |
|<span data-ttu-id="24142-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="24142-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="24142-110">Объекты таблиц серверов</span><span class="sxs-lookup"><span data-stu-id="24142-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="24142-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="24142-111">Called by:</span></span>  <br/> |<span data-ttu-id="24142-112">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="24142-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="24142-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="24142-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="24142-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="24142-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="24142-115">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="24142-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="24142-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="24142-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="24142-117">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="24142-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="24142-118">Transacted</span><span class="sxs-lookup"><span data-stu-id="24142-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="24142-119">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="24142-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="24142-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="24142-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="24142-121">Возвращает сведения о последней ошибке, которая произошла в объекте таблицы.</span><span class="sxs-lookup"><span data-stu-id="24142-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="24142-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="24142-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="24142-123">Возвращает указатель на интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="24142-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="24142-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="24142-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="24142-125">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="24142-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="24142-126">**Свойства, используемые для изменения таблицы правил**</span><span class="sxs-lookup"><span data-stu-id="24142-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="24142-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="24142-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24142-128">**PR_RULE_ACTIONS** ([PidTagRuleActions)](pidtagruleactions-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24142-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-132">**PR_RULE_ID** ([PidTagRuleId)](pidtagruleid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-134">**PR_RULE_LEVEL** ([PidTagRuleLevel)](pidtagrulelevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24142-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider)](pidtagruleprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData)](pidtagruleproviderdata-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence)](pidtagrulesequence-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24142-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags)](pidtagruleuserflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="24142-148">**Свойства, используемые для изменения таблицы SACL**</span><span class="sxs-lookup"><span data-stu-id="24142-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="24142-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="24142-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24142-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId)](pidtagmemberentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-152">**PR_MEMBER_ID** ([PidTagMemberId)](pidtagmemberid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="24142-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="24142-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights)](pidtagmemberrights-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="24142-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="24142-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="24142-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24142-158">Примечания</span><span class="sxs-lookup"><span data-stu-id="24142-158">Remarks</span></span>

<span data-ttu-id="24142-159">Чтобы получить интерфейс **IExchangeModifyTable,** вызовите метод MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) в свойстве типа PT_OBJECT объекте папки.</span><span class="sxs-lookup"><span data-stu-id="24142-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="24142-160">При вызове метода **OpenProperty** передав значение IID_IExchangeModifyTable _параметру lpiid._ </span><span class="sxs-lookup"><span data-stu-id="24142-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="24142-161">См. также</span><span class="sxs-lookup"><span data-stu-id="24142-161">See also</span></span>



[<span data-ttu-id="24142-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="24142-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

