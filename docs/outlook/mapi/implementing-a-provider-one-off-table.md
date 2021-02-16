---
title: Реализация таблицы One-Off поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436295"
---
# <a name="implementing-a-provider-one-off-table"></a>Реализация таблицы One-Off поставщика

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI вызывает метод [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) поставщика, когда пользователь клиентского приложения добавляет получателя в исходяное сообщение. Обычно запрашиваются уникальные типы адресов для системы обмена сообщениями. Если поставщик поддерживает создание получателей, он должен предоставить одностолевую таблицу, которая предоставляет шаблоны для каждого типа поддерживаемых адресов получателей. Если ваш поставщик не поддерживает создание получателей, MAPI_E_NO_SUPPORT из вызова **GetOneOffTable.** 
  
КАК правило, MAPI не будет открывать одноразовую таблицу поставщика в течение всего времени сеанса, освобождая ее только в том случае, если клиент вызывает метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) подсистемы или адресной книги. MAPI регистрирует уведомления в этой таблице, чтобы при добавлении или удалении шаблонов эти изменения могли быть отражены для пользователя. 
  
 **Реализация IABLogon::GetOneOffTable**
  
1. Проверьте значение параметра flags _ulFlags._ Если флаг MAPI_UNICODE установлен и поставщик не поддерживает Юникод, сбой и возврат MAPI_E_BAD_CHARWIDTH. 
    
2. Проверьте, создана ли односеаленная таблица поставщика. Так как разовые таблицы обычно являются статическими, поставщику никогда не нужно проходить процесс создания более одного раза. Если таблица уже существует, вернетесь на нее указателем. 
    
3. Если разовая таблица еще не существует, вызовите **CreateTable,** чтобы создать ее. 
    
4. Установите следующие свойства для столбцов в строках таблицы:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)на имя типа получателя, который шаблон может создать. 
    
  - **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)в идентификатор записи для одноразового шаблона.
    
  - **PR_DEPTH** ([PidTagDepth),](pidtagdepth-canonical-property.md)чтобы указать уровень иерархии в одноразовом табличе.
    
  - **PR_SELECTABLE** [(PidTagSelectable)](pidtagselectable-canonical-property.md)с true, чтобы указать, представляет ли строка шаблон, а false в противном случае.
    
  - **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)для типа адреса, созданного шаблоном.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)DT_MAILUSER или другое значение, которое указывает тип отображения шаблона.
    
  - **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)для уникального двоичного значения. 
    
5. Вызовите [ITableData::HrModifyRow,](itabledata-hrmodifyrow.md) чтобы изменить таблицу напрямую. 
    
6. Вызовите [ITableData::HrGetView,](itabledata-hrgetview.md) чтобы создать реализацию интерфейса **IMAPITable** для возврата вызываемой. 
    

