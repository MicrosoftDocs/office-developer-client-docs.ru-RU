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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Все поставщики услуг должны реализовать объект состояния и предоставить свойства из него в таблицу состояния сеанса. В таблицу состояния можно включить одну или несколько строк в зависимости от количества ресурсов, которые вы контролируете. Например, поставщик транспорта должен создать строку в таблице состояния для каждой управляемой им очереди сообщений. При внесении изменений необходимо обновить соответствующую строку таблицы состояния. Объекты status реализованы для предоставления доступа как к сведениям, включенным в таблицу состояния, так и к дополнительным сведениям, не включенным в таблицу.
  
### <a name="to-implement-a-status-object"></a>Реализация объекта состояния

1. Реализуйте **метод OpenStatusEntry** вашего объекта logon. Когда клиенты хотят открыть объект состояния, они называют [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI выполняет открытый запрос, вызывая метод **OpenStatusEntry** поставщика, в результате чего поставщик открывает объект состояния и возвращает клиенту указатель на реализацию **IMAPIStatus.** В реализации **OpenStatusEntry** выполните следующие действия: 
    
   1. Выполните следующие задачи, если объект logon еще не создал объект состояния:
    
      1. Вызов метода [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы получить доступ к разделу профилей поставщика. 
          
      2. Создайте новый объект состояния.
          
      3. Храните ссылку на раздел профилей в объекте состояния поставщика и позвоните в метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) чтобы приумновить количество ссылок. 
          
      4. Храните ссылку на объект logon в объекте состояния поставщика и позвоните в **метод IUnknown::AddRef,** чтобы приумновить его количество ссылок. 
          
      5. Храните ссылку на объект состояния в объекте logon поставщика.
    
   2. Вызов метода **IUnknown::AddRef** объекта состояния, чтобы приумновить количество ссылок в объекте logon. 
    
   3. Установите свойство PR_OBJECT_TYPE **объекта** состояния [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)для MAPI_STATUS.
    
   4. Установите параметр  _вывода lppMAPIStatus_ для указать на объект состояния и вернуться. 
    
   5. Проверьте параметр _ввода ulFlags._ Если установлено, MAPI_MODIFY и поставщик поддерживает доступ к объекту чтения и записи, возвращайте объект, который можно написать. Однако, если поставщик не поддерживает доступ к объекту чтения и записи, не сбой. Возвращайте объект состояния, который только для чтения. Клиенты, ожидающие получения объектов состояния чтения и записи, должны убедиться, что разрешение на чтение и записи было предоставлено, прежде чем пытаться внести какие-либо изменения. 
    
2. Установите все необходимые свойства объекта состояния и таблицы состояния. Свойства, которые вы включаете в строку таблицы состояния, должны быть доступны через объект состояния, за исключением свойств, рассчитанных по MAPI. Необходимые свойства:
    
   - **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
   - **PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)
    
   - **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
   - **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)
    
   - **PR_RESOURCE_METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)
    
   - **PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)
    
   - **PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)
    
3. Реализация [методов IMAPIStatus: IMAPIProp,](imapistatusimapiprop.md) подходящих вашему поставщику. В зависимости от поставщика не нужно внедрять все четыре метода **в IMAPIStatus.** Каждый поставщик должен реализовать только для чтения версию методов [интерфейса IMAPIProp : IUnknown](imapipropiunknown.md) и [метода IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 

   Поставщики транспорта также должны реализовать [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md)и все поставщики должны поддерживать [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). Однако поддержка [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) необязательна. Для реализации этого метода необходимо использовать только поставщиков услуг, которые требуют паролей и хотят разрешить пользователям изменять их программным путем. Для каждого поддерживаемого метода установите соответствующий бит в **свойстве PR_RESOURCE_METHODS.** Например, если вы поддерживаете **только ValidateState** и **SettingsDialog,** **PR_RESOURCE_METHODS** ниже: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Клиенты должны проверить значение **PR_RESOURCE_METHODS** перед попыткой вызвать объект состояния. Обрабатывайте вызовы к любому из неподтверченных методов, возвращая MAPI_E_NO_SUPPORT. 
    
4. Вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) во время логотипа, чтобы добавить строки или строки в таблицу состояния. Передай массив значений свойств, содержащий сведения столбца для строки и 0 для _параметра ulFlags._ Если в какой-то момент после сеанса состояние поставщика изменится и потребуется обновить сведения о столбце, снова позвоните **в ModifyStatusRow** с STATUSROW_UPDATE флагом. 
    
Дополнительные сведения об объектах состояния см. в [карте MAPI Status Objects.](mapi-status-objects.md)
  
## <a name="see-also"></a>См. также

- [Поставщики услуг MAPI](mapi-service-providers.md)

