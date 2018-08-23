---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 23663cea49c50f3f584d6b06e331545320e8283b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565384"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о состоянии о подсистемы MAPI, встроенная адресной книги и диспетчер очереди MAPI. Поставщик службы реализует **IMAPIStatus** для предоставления сведений о своем состоянии. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты состояния  <br/> |
|Реализованный:  <br/> |Поставщиков услуг и MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIStatus  <br/> |
|Тип указателя:  <br/> |LPMAPISTATUS  <br/> |
|Модель транзакций:  <br/> |Не входящих в транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Проверяет состояние внешних информация, доступная для ресурсов MAPI или поставщика услуг.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Отображает страницу свойств, который позволяет пользователю изменять конфигурации поставщика услуг.  <br/> |
|[Изменение пароля](imapistatus-changepassword.md) <br/> |Изменение пароля поставщика услуг без отображения пользовательского интерфейса.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Выполняет принудительное все сообщения, ожидающие отправку и получение для сразу же отправки или загрузки.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

Состояние объекты, внедряемые MAPI поддерживают следующие методы:
  
|**Состояние объекта**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |Только **ValidateState**  <br/> |
|Адресная книга MAPI  <br/> |Только **ValidateState**  <br/> |
|Диспетчер очереди MAPI  <br/> |**ValidateState** и **FlushQueues** <br/> |
   
Состояние объекты, внедряемые MAPI должны иметь только для чтения версии методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддерживает метод **ValidateState** . Поставщики транспорта, также должны поддерживать **FlushQueues**. Все поставщики должны поддерживать **SettingsDialog**; Поддержка **Изменение пароля** является необязательным. 
  
Клиенты используют объекты состояние для выполнения настройки, а также информацию о состоянии сеанса. Они доступ к объекту состояния путем вызова метода **OpenStatusEntry** объекта службы поставщика входа в систему или метод [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для извлечения объекта состояния. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

