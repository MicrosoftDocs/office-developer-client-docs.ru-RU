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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336339"
---
# <a name="status-object-implementation"></a>Реализация объекта состояния

**Относится к**: Outlook 2013 | Outlook 2016 
  
Все поставщики услуг должны реализовать объект состояния и предоставить из него свойства в таблицу состояния сеанса. В таблицу состояния можно включить одну или несколько строк в зависимости от количества ресурсов, которые вы контролируете. Например, поставщик транспорта должен создать строку в таблице состояния для каждой управляемой им очереди сообщений. При внесении изменений необходимо обновить соответствующую строку таблицы состояния. Объекты состояния реализуются для предоставления доступа как к сведениям, включенным в таблицу состояния, так и к дополнительным сведениям, не включенным в таблицу.
  
### <a name="to-implement-a-status-object"></a>Реализация объекта состояния

1. Реализуйте **метод OpenStatusEntry** объекта для логотипа. Когда клиенты хотят открыть объект состояния, они [вызовят IMAPISession::OpenEntry.](imapisession-openentry.md) MAPI выполняет открытый запрос, вызывая метод Вашего поставщика **OpenStatusEntry,** в результате чего поставщик открывает объект состояния и возвращает клиенту указатель на реализацию **IMAPIStatus.** В **реализации OpenStatusEntry** выполните следующие действия: 
    
   1. Выполните следующие задачи, если объект для логотипа еще не создал объект состояния:
    
      1. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы получить доступ к разделу профиля поставщика. 
          
      2. Создание объекта состояния.
          
      3. Храните ссылку на раздел профиля в объекте состояния поставщика и вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) раздела профиля, чтобы помность его количество ссылок. 
          
      4. Храните ссылку на объект для логотипа в объекте состояния вашего поставщика и вызовите метод **IUnknown::AddRef** объекта для инкрементного инкрементного подсчета ссылок. 
          
      5. Храните ссылку на объект status в объекте для логотипа поставщика.
    
   2. Вызовите метод **IUnknown::AddRef** объекта состояния для инкрементного подсчета ссылок в объекте для логотипа. 
    
   3. Установите для свойства PR_OBJECT_TYPE объекта **PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)MAPI_STATUS.
    
   4. Задан  _выходной параметр lppMAPIStatus_ для указать на объект состояния и вернуться. 
    
   5. Проверьте _входной параметр ulFlags._ Если установлено MAPI_MODIFY и ваш поставщик поддерживает доступ на чтение и записи к объекту состояния, возвращает объект, доступный для записи. Однако если поставщик не поддерживает доступ на чтение и записи к объекту состояния, не сделайте этого. Возвращает объект состояния, который является только для чтения. Клиенты, которые ожидают получения объектов состояния чтения и записи, должны убедиться, что разрешение на чтение и записи предоставлено, прежде чем пытаться внести какие-либо изменения. 
    
2. Установите все необходимые свойства объекта состояния и таблицы состояния. Свойства, которые вы включаете в строку таблицы состояния, должны быть доступны через объект состояния, за исключением свойств, вычисляемого с помощью MAPI. Необходимые свойства:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)
    
   - **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)
    
3. Реализуйте [методы IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) подходящие для вашего поставщика. В зависимости от поставщика вам не нужно реализовывать все четыре метода **в IMAPIStatus.** Каждый поставщик должен реализовать версию методов [интерфейса IMAPIProp : IUnknown](imapipropiunknown.md) и [метода IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 

   Поставщики транспорта также должны реализовать [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md)а все поставщики должны поддерживать [IMAPIStatus::SettingsDialog.](imapistatus-settingsdialog.md) Однако поддержка [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) является необязательной. Этот метод необходимо реализовать только тем поставщикам служб, которые требуют паролей и хотят разрешить пользователям изменять их программным способом. Для каждого поддерживаемого метода установите соответствующий бит в свойстве **PR_RESOURCE_METHODS.** Например, если вы поддерживаете **только ValidateState** и **SettingsDialog,** PR_RESOURCE_METHODS **следующие** параметры: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Клиенты должны проверять значение **PR_RESOURCE_METHODS** перед попыткой вызова объекта состояния. Обрабатывайте вызовы любого из неподтверченных методов, возвращая MAPI_E_NO_SUPPORT. 
    
4. Вызовите [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) во время логотипа, чтобы добавить строки или строки в таблицу состояния. Передав массив значений свойств, содержащий сведения о столбцах для строки и 0 для _параметра ulFlags._ Если в определенный момент позднее в сеансе состояние поставщика изменится и потребуется обновить сведения о столбце, снова вызовите **ModifyStatusRow** с установленным STATUSROW_UPDATE флагом. 
    
Дополнительные сведения об объектах состояния см. в поддоме ["Объекты состояния MAPI".](mapi-status-objects.md)
  
## <a name="see-also"></a>См. также

- [Поставщики услуг MAPI](mapi-service-providers.md)

