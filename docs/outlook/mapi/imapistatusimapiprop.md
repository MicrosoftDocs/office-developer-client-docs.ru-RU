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
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408301"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о состоянии подсистемы MAPI, интегрированной адресной книги и шпалере MAPI. Поставщик услуг реализует **IMAPIStatus,** чтобы предоставить сведения о своем собственном состоянии. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты состояний  <br/> |
|Реализовано в:  <br/> |Поставщики услуг и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIStatus  <br/> |
|Тип указателя:  <br/> |LPMAPISTATUS  <br/> |
|Модель транзакции:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Подтверждает сведения о внешнем состоянии, доступные для ресурса MAPI или поставщика услуг.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Отображает лист свойств, который позволяет пользователю изменять конфигурацию поставщика услуг.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Изменяет пароль поставщика услуг без отображения пользовательского интерфейса.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Заставляет все сообщения, ожидаемые для отправки или отправки, немедленно загружаться или загружаться.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Объекты состояния, реализуемые MAPI, поддерживают следующие методы:
  
|**Объект Status**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |**Только ValidateState**  <br/> |
|Адресная книга MAPI  <br/> |**Только ValidateState**  <br/> |
|Шпалер MAPI  <br/> |**ValidateState** и **FlushQueues** <br/> |
   
Объекты состояния, реализуемые MAPI, должны иметь только для чтения версию методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддерживать метод **ValidateState.** Поставщики транспорта также должны поддерживать **flushQueues.** Все поставщики должны поддерживать **SettingsDialog;** поддержка **ChangePassword** необязательна. 
  
Клиенты используют объекты состояния для выполнения конфигурации и для того, чтобы узнать о состоянии сеанса. Они получают доступ к объекту состояния, позвонив **методу OpenStatusEntry** объекта logon поставщика услуг или [методу IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения объекта состояния. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

