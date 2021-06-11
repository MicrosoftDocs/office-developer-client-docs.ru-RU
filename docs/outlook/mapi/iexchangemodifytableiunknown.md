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
# <a name="iexchangemodifytable--iunknown"></a><span data-ttu-id="5c248-103">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c248-103">IExchangeModifyTable : IUnknown</span></span>

  
  
<span data-ttu-id="5c248-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c248-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c248-105">Поддерживает доступ к Microsoft Exchange Server, в частности к объектам таблицы управления доступом системы (SACL) и объектам таблицы правил в Microsoft Exchange Server папках.</span><span class="sxs-lookup"><span data-stu-id="5c248-105">Supports access to Microsoft Exchange Server table objects, specifically system access control list (SACL) table objects and rule table objects on Microsoft Exchange Server folders.</span></span> <span data-ttu-id="5c248-106">Этот интерфейс похож на интерфейс [IMAPITable : IUnknown,](imapitableiunknown.md) но он добавляет поддержку Microsoft Exchange Server структур, используемых для управления SACLs и правилами.</span><span class="sxs-lookup"><span data-stu-id="5c248-106">This interface resembles the [IMAPITable : IUnknown](imapitableiunknown.md) interface, but it adds support for Microsoft Exchange Server-specific structures that are used to control SACLs and rules.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c248-107">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="5c248-107">Exposed by:</span></span>  <br/> |<span data-ttu-id="5c248-108">Нет</span><span class="sxs-lookup"><span data-stu-id="5c248-108">None</span></span>  <br/> |
|<span data-ttu-id="5c248-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5c248-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c248-110">Объекты таблицы сервера</span><span class="sxs-lookup"><span data-stu-id="5c248-110">Server table objects</span></span>  <br/> |
|<span data-ttu-id="5c248-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5c248-111">Called by:</span></span>  <br/> |<span data-ttu-id="5c248-112">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="5c248-112">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="5c248-113">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5c248-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5c248-114">IID_IExchangeModifyTable</span><span class="sxs-lookup"><span data-stu-id="5c248-114">IID_IExchangeModifyTable</span></span>  <br/> |
|<span data-ttu-id="5c248-115">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="5c248-115">Pointer type:</span></span>  <br/> |<span data-ttu-id="5c248-116">LPEXCHANGEMODIFYTABLE</span><span class="sxs-lookup"><span data-stu-id="5c248-116">LPEXCHANGEMODIFYTABLE</span></span>  <br/> |
|<span data-ttu-id="5c248-117">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="5c248-117">Transaction model:</span></span>  <br/> |<span data-ttu-id="5c248-118">Transacted</span><span class="sxs-lookup"><span data-stu-id="5c248-118">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5c248-119">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="5c248-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5c248-120">GetLastError</span><span class="sxs-lookup"><span data-stu-id="5c248-120">GetLastError</span></span>](iexchangemodifytable-getlasterror.md) <br/> |<span data-ttu-id="5c248-121">Возвращает сведения о последней ошибке, которая произошла в объекте таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c248-121">Returns information about the last error that occurred in a table object.</span></span>  <br/> |
|[<span data-ttu-id="5c248-122">GetTable</span><span class="sxs-lookup"><span data-stu-id="5c248-122">GetTable</span></span>](iexchangemodifytable-gettable.md) <br/> |<span data-ttu-id="5c248-123">Возвращает указатель в интерфейс для объекта таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c248-123">Returns a pointer to an interface for a MAPI table object.</span></span>  <br/> |
|[<span data-ttu-id="5c248-124">ModifyTable</span><span class="sxs-lookup"><span data-stu-id="5c248-124">ModifyTable</span></span>](iexchangemodifytable-modifytable.md) <br/> |<span data-ttu-id="5c248-125">Обновляет объект таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c248-125">Updates a MAPI table object.</span></span>  <br/> |
   
|<span data-ttu-id="5c248-126">**Свойства, используемые для изменения таблицы правил**</span><span class="sxs-lookup"><span data-stu-id="5c248-126">**Properties used to modify a rules table**</span></span>|<span data-ttu-id="5c248-127">**Access**</span><span class="sxs-lookup"><span data-stu-id="5c248-127">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c248-128">**PR_RULE_ACTIONS** [(PidTagRuleActions)](pidtagruleactions-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-128">**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-129">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-130">**PR_RULE_CONDITION** [(PidTagRuleCondition)](pidtagrulecondition-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-130">**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-132">**PR_RULE_ID** [(PidTagRuleId)](pidtagruleid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-132">**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-133">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-134">**PR_RULE_LEVEL** [(PidTagRuleLevel)](pidtagrulelevel-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-134">**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-136">**PR_RULE_NAME** [(PidTagRuleName)](pidtagrulename-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-136">**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-138">**PR_RULE_PROVIDER** [(PidTagRuleProvider)](pidtagruleprovider-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-138">**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-140">**PR_RULE_PROVIDER_DATA** [(PidTagRuleProviderData)](pidtagruleproviderdata-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-140">**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-141">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-142">**PR_RULE_SEQUENCE** [(PidTagRuleSequence)](pidtagrulesequence-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-142">**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-143">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-144">**PR_RULE_STATE** [(PidTagRuleState)](pidtagrulestate-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-144">**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-145">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-146">**PR_RULE_USER_FLAGS** [(PidTagRuleUserFlags)](pidtagruleuserflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-146">**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-147">Read-only</span></span>  <br/> |
   
|<span data-ttu-id="5c248-148">**Свойства, используемые для изменения таблицы SACL**</span><span class="sxs-lookup"><span data-stu-id="5c248-148">**Properties used to modify a SACL table**</span></span>|<span data-ttu-id="5c248-149">**Access**</span><span class="sxs-lookup"><span data-stu-id="5c248-149">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c248-150">**PR_MEMBER_ENTRYID** [(PidTagMemberEntryId)](pidtagmemberentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-150">**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-151">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-151">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-152">**PR_MEMBER_ID** [(PidTagMemberId)](pidtagmemberid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-152">**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-153">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-153">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-154">**PR_MEMBER_NAME** [(PidTagMemberName)](pidtagmembername-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-154">**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-155">Read-only</span></span>  <br/> |
|<span data-ttu-id="5c248-156">**PR_MEMBER_RIGHTS** [(PidTagMemberRights)](pidtagmemberrights-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="5c248-156">**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5c248-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c248-157">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c248-158">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c248-158">Remarks</span></span>

<span data-ttu-id="5c248-159">Чтобы получить **интерфейс IExchangeModifyTable,** позвоните в метод MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с свойством типа PT_OBJECT на объекте папки.</span><span class="sxs-lookup"><span data-stu-id="5c248-159">To obtain the **IExchangeModifyTable** interface, call the MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method on a property of type PT_OBJECT on a folder object.</span></span> <span data-ttu-id="5c248-160">При вызове **метода OpenProperty** передай **значение** IID_IExchangeModifyTable в _параметре lpiid._</span><span class="sxs-lookup"><span data-stu-id="5c248-160">When you call the **OpenProperty** method, pass the value **IID_IExchangeModifyTable** in the  _lpiid_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5c248-161">См. также</span><span class="sxs-lookup"><span data-stu-id="5c248-161">See also</span></span>



[<span data-ttu-id="5c248-162">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="5c248-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

