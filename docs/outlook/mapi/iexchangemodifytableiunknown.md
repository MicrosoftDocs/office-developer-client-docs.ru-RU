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
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поддерживает доступ к объектам в таблице Microsoft Exchange Server, в частности доступа к системе управления список управления ДОСТУПОМ в таблице объекты и правила в таблице объекты на папок Microsoft Exchange Server. Имеет следующий вид: этот интерфейс [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса, но он обеспечивает поддержку структуры специфичных для сервера Microsoft Exchange, которые используются для управления доступом и правила. 
  
|||
|:-----|:-----|
|Предоставляемые:  <br/> |Отсутствует  <br/> |
|Реализованный:  <br/> |В таблице объекты сервера  <br/> |
|Вызывается:  <br/> |MAPI и клиентских приложениях  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IExchangeModifyTable  <br/> |
|Тип указателя:  <br/> |LPEXCHANGEMODIFYTABLE  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Возвращает сведения о, последнюю ошибку в объекте таблицы.  <br/> |
|[Соответствие доступному](iexchangemodifytable-gettable.md) <br/> |Возвращает указатель на интерфейс для объекта таблицы MAPI.  <br/> |
|[ModifyTable](iexchangemodifytable-modifytable.md) <br/> |Обновляет объект таблицы MAPI.  <br/> |
   
|**Свойства, используемые для изменения таблицы правил**|**Access**|
|:-----|:-----|
|**PR_RULE_ACTIONS** ([PidTagRuleActions](pidtagruleactions-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_CONDITION** ([PidTagRuleCondition](pidtagrulecondition-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_ID** ([PidTagRuleId](pidtagruleid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_LEVEL** ([PidTagRuleLevel](pidtagrulelevel-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_NAME** ([PidTagRuleName](pidtagrulename-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_PROVIDER** ([PidTagRuleProvider](pidtagruleprovider-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_PROVIDER_DATA** ([PidTagRuleProviderData](pidtagruleproviderdata-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_SEQUENCE** ([PidTagRuleSequence](pidtagrulesequence-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_STATE** ([PidTagRuleState](pidtagrulestate-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RULE_USER_FLAGS** ([PidTagRuleUserFlags](pidtagruleuserflags-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
|**Свойства, используемые для изменения таблицы системный список управления ДОСТУПОМ**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить интерфейс **IExchangeModifyTable** , вызовите метод MAPI [IMAPIProp::OpenProperty](imapiprop-openproperty.md) на свойство типа PT_OBJECT на объект folder. При вызове метода **OpenProperty** передайте значение **IID_IExchangeModifyTable** с помощью параметра _lpiid_ . 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

