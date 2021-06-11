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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI вызывает метод [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) поставщика, когда пользователь клиентского приложения добавляет получателя в исходяние сообщение. Как правило, типы запрашиваемого адреса уникальны для системы обмена сообщениями. Если поставщик поддерживает создание получателей, он должен предоставить разовую таблицу, которая предоставляет шаблоны для каждого типа поддерживаемого адреса получателя. Если поставщик не поддерживает создание получателей, MAPI_E_NO_SUPPORT из **вызова GetOneOffTable.** 
  
MapI обычно будет держать разовую таблицу поставщика открытой на весь срок действия сеанса, выпуская ее только тогда, когда клиент вызывает метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) подсистемы или адресной книги. MAPI регистрирует уведомления на этой таблице, чтобы при добавлении или удалении шаблонов эти изменения могли быть отражены пользователю. 
  
 **Реализация IABLogon::GetOneOffTable**
  
1. Проверьте значение параметра флаги  _ulFlags_. Если флаг MAPI_UNICODE установлен и поставщик не поддерживает Unicode, сбой и возвращение MAPI_E_BAD_CHARWIDTH. 
    
2. Проверьте, создана ли разовая таблица поставщика. Поскольку разовые таблицы обычно являются статичными, поставщику никогда не нужно проходить процесс создания более одного раза. Если таблица уже существует, верни указатель в нее. 
    
3. Если разовая таблица еще не существует, позвоните **в CreateTable,** чтобы создать ее. 
    
4. Установите следующие свойства для столбцов в строках таблицы:
    
  - **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)имени типа получателя, который может создать шаблон. 
    
  - **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)к идентификатору записи для разового шаблона.
    
  - **PR_DEPTH** [(PidTagDepth),](pidtagdepth-canonical-property.md)чтобы указать уровень иерархии в разовом дисплее таблицы.
    
  - **PR_SELECTABLE** [(PidTagSelectable)](pidtagselectable-canonical-property.md)для TRUE, чтобы указать, представляет ли строка шаблон, а false — иначе.
    
  - **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)для типа адреса, созданного шаблоном.
    
  - **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)для DT_MAILUSER или другого значения, которое указывает тип отображения шаблона.
    
  - **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)к уникальному двоичному значению. 
    
5. Вызов [ITableData::HrModifyRow,](itabledata-hrmodifyrow.md) чтобы изменить таблицу напрямую. 
    
6. Вызов [ITableData::HrGetView](itabledata-hrgetview.md) для создания **реализации интерфейса IMAPITable,** чтобы вернуться к вызываемой. 
    

