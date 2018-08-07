---
title: Реализация одноразовой таблицы поставщиков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809300"
---
# <a name="implementing-a-provider-one-off-table"></a>Реализация одноразовой таблицы поставщиков

  
  
**Относится к**: Outlook 
  
MAPI вызывает метод [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) ваш поставщик, когда пользователь клиентское приложение добавляет получателя для исходящих сообщений. Как правило типы адресов запрошено являются уникальными для обмена сообщениями в системе. Если ваш поставщик поддерживает создание получателей, оно должно поддерживать одноразовых таблица, в которой предоставляет шаблоны для каждого типа поддерживаемых адрес получателя. Если ваш поставщик не поддерживает создание получателей, возвратите MAPI_E_NO_SUPPORT из **GetOneOffTable** вызова. 
  
MAPI обычно будет закрывайте ваш поставщик одноразовых таблицы для сеанса, освобождая его только в том случае, если клиент вызывает либо подсистемы или адресной книги [IMAPIStatus::ValidateState](imapistatus-validatestate.md) метод. MAPI регистрирует уведомлений на этой таблице, чтобы при добавлении или удалении шаблонов, эти изменения могут быть отражены для пользователя. 
  
 **Для реализации IABLogon::GetOneOffTable**
  
1. Проверьте значение параметра флаги, _ulFlags_. Если задан флаг MAPI_UNICODE и ваш поставщик не поддерживает Юникод, с ошибкой и возвращают MAPI_E_BAD_CHARWIDTH. 
    
2. Установите флажок, если ваш поставщик одноразовых таблица еще создана. Поскольку одноразовых таблиц, обычно static, ваш поставщик не может пройти через процесс создания более одного раза. Если таблица уже существует, возвращает указатель на него. 
    
3. Если одноразовых таблица еще не существует, вызовите **CreateTable** для его создания. 
    
4. Задайте следующие свойства для столбцов в строк таблицы:
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) к имени типа получателя, который можно создать шаблон. 
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) с идентификатором записи для одноразовых шаблона.
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) для определения уровня иерархии в отображении одноразовых таблицы.
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) значение TRUE, чтобы указать, если строка представляет шаблон и значение FALSE в противном случае.
    
  - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) тип адреса, создаваемых в шаблоне.
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER или другое значение, указывающее тип отображения для шаблона.
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) уникальный двоичное значение. 
    
5. Вызов [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) для изменения непосредственно в таблице. 
    
6. Вызов [ITableData::HrGetView](itabledata-hrgetview.md) для создания реализация интерфейса **IMAPITable** , чтобы вернуться к вызывающему. 
    

