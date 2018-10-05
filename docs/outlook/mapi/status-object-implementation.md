---
title: Реализация объекта состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392405"
---
# <a name="status-object-implementation"></a>Реализация объекта состояния

**Относится к**: Outlook 2013 | Outlook 2016 
  
Все поставщики услуг необходимо реализовать объект состояния и предоставлять свойства из его в таблице состояния сеанса. В таблице состояния, в зависимости от количества ресурсов, которые можно управлять может включать один или несколько строк. Например, поставщика транспорта, необходимо создать строку в таблице состояния для каждого управляемого очереди сообщений. При внесении изменений, необходимо обновить строка таблицы соответствующего состояния. Состояние объекты реализованы для предоставления доступа к данным, включенные в таблице состояния и на дополнительные сведения, не включенные в таблице.
  
### <a name="to-implement-a-status-object"></a>Для реализации объекта состояния

1. Реализуйте метод **OpenStatusEntry** объекта входа в систему. Если клиентам требуется открыть состояние объекта, он совершает вызов [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI выполняет открыть запрос, вызвав метод **OpenStatusEntry** ваш поставщик, вызывает поставщика для открытия его состояние объекта и вернуться к клиенту указатель на его реализация **IMAPIStatus** . В реализации **OpenStatusEntry** выполните следующие действия: 
    
   1. Если объект входа еще не создан объект состояния выполнения следующих задач:
    
      1. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки для доступа к раздела профиля ваш поставщик. 
          
      2. Создайте новый объект состояния.
          
      3. Хранить ссылку на раздел профиля в ваш поставщик состояние объекта и вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) раздела профиля увеличить счетчик ссылок на него. 
          
      4. Сохранить ссылку на объект входа в ваш поставщик состояние объекта и вызовите метод **IUnknown::AddRef** объекта входа для увеличения счетчик ссылок на него. 
          
      5. Сохраните ссылку на объект состояния в объект вашего поставщика входа в систему.
    
   2. Вызовите метод **IUnknown::AddRef** состояние объекта увеличить счетчик ссылок на него в объект вход в систему. 
    
   3. Состояние объекта **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) для свойства MAPI_STATUS.
    
   4. Установите для параметра _lppMAPIStatus_ выходные данные для команды объект состояния и возврата. 
    
   5. Установите флажок _ulFlags_ входного параметра. Если задано значение MAPI_MODIFY и ваш поставщик поддерживает чтение и запись доступа к его состояние объекта, возвращают объект доступным для записи. Тем не менее если ваш поставщик не поддерживает чтение и запись доступа к его состояние объекта, не с ошибкой. Возвращает объект состояния, который доступен только для чтения. Клиенты, которые согласно прогнозу, будут получать объекты состояние чтения/записи необходимо проверить предоставления разрешений на чтение/запись перед попыткой внесите изменения. 
    
2. Задайте все необходимые состояние объекта и состояния в таблице. Свойства, включая ваше состояние строки в таблице должны быть доступны через объект состояния, за исключением свойства рассчитать с MAPI. Необходимые свойства, как показано ниже:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Реализация [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) методы, которые подходят для поставщика. В зависимости от поставщика не требуется реализовать все четыре метода в **IMAPIStatus**. Каждый поставщик должен реализовывать только для чтения версии методов для [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейс и метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 

   Поставщики транспорта также требуется реализовать [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)и всех поставщиков должны поддерживать [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). Тем не менее поддержка [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) является необязательным. Для реализации этого метода требуются только поставщиков услуг, использующих пароли, которые требуется разрешить пользователям изменять их программными средствами. Для каждого метода, который поддерживается установите соответствующий бит в свойстве **PR_RESOURCE_METHODS** . Например если вы поддерживаете **ValidateState** и **SettingsDialog** только, задайте для **PR_RESOURCE_METHODS** следующее: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Клиенты должен проверить значение **PR_RESOURCE_METHODS** , прежде чем для вызова состояние объекта. Обработка звонков на любой из неподдерживаемых методов, возвращая MAPI_E_NO_SUPPORT. 
    
4. Вызовите [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) во время входа в систему для добавления строки или строк в таблице состояния. Передача массива значение свойства, которое содержит сведения о столбце для строки и 0 для параметра _ulFlags_ . Если по какой-то момент в сеансе изменения состояния вашего поставщика и его необходимо обновить данные столбца, вызовите **ModifyStatusRow** еще раз с установленным флагом STATUSROW_UPDATE. 
    
Дополнительные сведения о состоянии объекты видеть [Состояние объектов MAPI](mapi-status-objects.md).
  
## <a name="see-also"></a>См. также

- [Поставщиков служб MAPI](mapi-service-providers.md)

