---
title: Имапистатус IMAPIProp
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения о состоянии подсистемы MAPI, интегрированной адресной книги и диспетчере очереди MAPI. Поставщик услуг реализует **имапистатус** для предоставления сведений о своем состоянии. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объекты состояний  <br/> |
|Реализовано в:  <br/> |Поставщики услуг и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIStatus  <br/> |
|Тип указателя:  <br/> |лпмапистатус  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[валидатестате](imapistatus-validatestate.md) <br/> |Проверяет внешние сведения о состоянии, доступные для ресурса MAPI или поставщика услуг.  <br/> |
|[сеттингсдиалог](imapistatus-settingsdialog.md) <br/> |Отображает страницу свойств, позволяющую пользователю изменить конфигурацию поставщика услуг.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Изменяет пароль поставщика услуг без отображения пользовательского интерфейса.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Принудительно отправляет или загружает все сообщения, ожидающие отправки или получения.  <br/> |
   
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

Объекты состояния, реализованные в MAPI, поддерживают следующие методы:
  
|**Объект Status**|**Поддерживаемые методы**|
|:-----|:-----|
|Подсистема MAPI  <br/> |Только **валидатестате**  <br/> |
|Адресная книга MAPI  <br/> |Только **валидатестате**  <br/> |
|Диспетчер очереди MAPI  <br/> |**Валидатестате** и **FlushQueues** <br/> |
   
Для объектов status, реализованных в MAPI, необходима доступная только для чтения версия методов интерфейса [IMAPIProp](imapipropiunknown.md) и поддержка метода **валидатестате** . Поставщики транспорта также должны поддерживать **FlushQueues**. Все поставщики должны поддерживать **сеттингсдиалог**; поддержка **ChangePassword** является необязательной. 
  
Клиенты используют объекты состояния для выполнения настройки и получения сведений о состоянии сеанса. Они обращаются к объекту status, вызывая метод **опенстатусентри** объекта входа поставщика услуг или метод [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для получения объекта Status. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

