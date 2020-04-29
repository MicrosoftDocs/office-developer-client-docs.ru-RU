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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418108"
---
# <a name="iexchangemodifytable--iunknown"></a>IExchangeModifyTable : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поддерживает доступ к объектам таблицы Microsoft Exchange Server, а именно к объектам таблицы и объектам таблицы правил списка управления доступом в папках Microsoft Exchange Server. Этот интерфейс напоминает интерфейс [IMAPITable: IUnknown](imapitableiunknown.md) , но он добавляет поддержку для отдельных структур Microsoft Exchange Server, которые используются для управления таблицами управления доступом и правилами. 
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Нет  <br/> |
|Реализовано в:  <br/> |Объекты таблицы сервера  <br/> |
|Вызывающая сторона:  <br/> |MAPI и клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IExchangeModifyTable  <br/> |
|Тип указателя:  <br/> |лпексчанжемодифитабле  <br/> |
|Модель транзакции:  <br/> |Транзакции  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](iexchangemodifytable-getlasterror.md) <br/> |Возвращает сведения о последней ошибке, произошедшей в объекте Table.  <br/> |
|[GetTable](iexchangemodifytable-gettable.md) <br/> |Возвращает указатель на интерфейс для объекта таблицы MAPI.  <br/> |
|[модифитабле](iexchangemodifytable-modifytable.md) <br/> |Обновляет объект таблицы MAPI.  <br/> |
   
|**Свойства, используемые для изменения таблицы Rules**|**Access**|
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
   
|**Свойства, используемые для изменения таблицы SACL**|**Access**|
|:-----|:-----|
|**PR_MEMBER_ENTRYID** ([PidTagMemberEntryId](pidtagmemberentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_ID** ([PidTagMemberId](pidtagmemberid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_NAME** ([PidTagMemberName](pidtagmembername-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_MEMBER_RIGHTS** ([PidTagMemberRights](pidtagmemberrights-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить интерфейс **иексчанжемодифитабле** , вызовите метод MAPI [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для свойства типа PT_OBJECT объекта Folder. При вызове метода **опенпроперти** передайте значение **IID_IExchangeModifyTable** в параметр _лпиид_ . 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

