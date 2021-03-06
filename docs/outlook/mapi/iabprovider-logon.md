---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348785"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает подключение к активному сеансу.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> [in] Указатель на объект поддержки поставщика адресной книги.
    
 _ulUIParam_
  
> [in] Ручка родительского окна для диалогового окна logon, отображаемого методом **Logon,** если разрешено. Параметр _ulUIParam_ содержит значение параметра с таким же именем, переданного MAPI в предыдущем вызове на функцию [MAPILogonEx.](mapilogonex.md) 
    
 _lpszProfileName_
  
> [in] Указатель на имя профиля сеанса.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют выполнение логотипа. Можно установить следующие флаги:
    
AB_NO_DIALOG 
  
> Поставщик не должен отображать диалоговое окно во время logon. Если этот флаг не установлен, поставщик может отобразить диалоговое окно, чтобы подсказыть пользователю отсутствующие сведения о конфигурации.
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **logon** успешно возвращаться, возможно, до завершения процесса логона. 
    
MAPI_UNICODE 
  
> Все строки должны быть в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.
    
 _lpulcbSecurity_
  
> [in, out] Указатель на размер в bytes структуры учетных данных безопасности, на который указывает параметр _lppbSecurity._ При входе значение должно быть незеро; на выходе значение должно быть нулевым. В обоих случаях указатели должны быть действительными. 
    
 _lppbSecurity_
  
> [in, out] Указатель на указатель на учетные данные безопасности. При входе значение должно быть незеро; на выходе значение должно быть нулевым. В обоих случаях указатель должен быть допустимым.
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на [структуру MAPIERROR.](mapierror.md) Параметр  _lppMAPIError может_ быть задан в NULL, если нет структуры **MAPIERROR** для возврата. 
    
 _lppABLogon_
  
> [вышел] Указатель на указатель на объект logon поставщика.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно установлено подключение к активному сеансу.
    
MAPI_E_FAILONEPROVIDER 
  
> Поставщик не может войти в систему, но MAPI может продолжать входить в систему других поставщиков в службе сообщений, к которой принадлежит поставщик. 
    
MAPI_E_UNCONFIGURED 
  
> У поставщика недостаточно сведений для завершения логотипа. MAPI вызывает функцию входа в службу сообщений поставщика.
    
MAPI_E_UNKNOWN_CPID 
  
> Сервер не настроен для поддержки страницы кода клиента.
    
MAPI_E_UNKNOWN_LCID 
  
> Сервер не настроен для поддержки сведений о локальном уровне клиента.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне logon. 
    
## <a name="remarks"></a>Примечания

Подключения устанавливаются с каждым поставщиком адресной книги в профиле сеанса, когда клиент вызывает [метод IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md) **Затем OpenAddressBook** вызывает метод **Logon каждого** поставщика. 
  
Имя профиля, на которое указывает параметр _lpszProfileName,_ отображается в наборе символов клиента пользователя, как указывается наличием или отсутствием флага MAPI_UNICODE в параметре _ulFlags._ 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

В реализации метода **Logon** вызывайте [метод IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или [структуры MAPIUID.](mapiuid.md) Каждый из ваших объектов будет иметь идентификатор записи, который включает этот **MAPIUID**. MAPI использует **MAPIUID** для совпадения объекта со своим поставщиком. Например, когда клиент вызывает метод [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия пользователя обмена сообщениями, **OpenEntry** проверяет часть **MAPIUID** идентификатора записи, которая была передана, и соотнося ее с **MAPIUID,** зарегистрированным поставщиком адресной книги. 
  
Если клиент входит в систему поставщика несколько раз, вам может потребоваться зарегистрировать другой **MAPIUID** для каждого логотипа. Регистрация уникальных **структур MAPIUID** позволяет MAPI правильно маршрутировать запросы в соответствующий экземпляр поставщика. Однако может потребоваться, чтобы каждый объект с логотипом делил **по одному MAPIUID.** В этом случае вы должны иметь возможность самостоятельно обрабатывать маршрутику, а не полагаться на MAPI. Дополнительные сведения о создании **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)
  
Объект поддержки, который MAPI передает методу **Logon** в _параметре lpMAPISup,_ предоставляет доступ ко многим методам, включенным в [интерфейс IMAPISupport : IUnknown.](imapisupportiunknown.md) MAPI создает объект поддержки, настраиваемый под ваш тип поставщика. Например, если при создании подключения необходимо войти в систему или службу каталогов, можно вызвать [метод IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md) чтобы получить учетные данные безопасности для этого конкретного сеанса логотипа. 
  
Если **logon** успешно, убедитесь, что вы вызываете метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы приумновить его количество ссылок. Это позволяет поставщику держаться за указатель объекта поддержки до конца сеанса. Если этот метод **AddRef** не называется, MAPI разгрузит поставщика. 
  
Имя профиля, переданное в  _параметре lpszProfileName,_ можно включить в диалоговые окна ошибок, экраны логотипов или другие пользовательские интерфейсы. Чтобы использовать имя профиля, скопируйте его в выделенное хранилище. 
  
Создайте объект logon и верни ему указатель в _параметре lppABLogon._ MAPI использует этот объект logon для звонков к методам реализации [IABLogon.](iablogoniunknown.md) 
  
Если во время логотипа требуется пароль, отобразите диалоговое окно с логотипом только в том случае, если AB_NO_DIALOG флаг не установлен. Если пользователь отменяет процесс логотипа, как правило, нажав кнопку Отмена в диалоговом окне, MAPI_E_USER_CANCEL **из Logon**. 
  
Как правило, если поставщик адресной книги не может войти в систему, MAPI отключает службу сообщений, к которой принадлежит поставщик сбоя, то есть MAPI не будет пытаться установить подключения для других поставщиков, которые относятся к службе до конца срока службы сеанса. Однако, если поставщик не может установить подключение и вы не хотите отключить всю службу, возвращайте MAPI_E_FAILONEPROVIDER или MAPI_E_UNCONFIGURED. MAPI не отключит службу сообщений, к которой принадлежит поставщик. 
  
Возврат MAPI_E_FAILONEPROVIDER, если возникает ошибка, которая не является достаточно серьезной, чтобы предотвратить установление подключений другими поставщиками в службе сообщений. Возвращайте MAPI_E_UNCONFIGURED, если из профиля отсутствуют необходимые сведения о конфигурации, и вы не можете отобразить диалоговое окно для запроса пользователя. MAPI будет отвечать, вызывая функцию точки входа службы сообщений поставщика с помощью MSG_SERVICE_CONFIGURE  _параметра ulContext,_ чтобы предоставить службе возможность настроить себя, программным образом или с помощью листа свойств. По завершению функции точки входа службы сообщений MAPI повторно вырисовывает логотип. 
  
## <a name="see-also"></a>См. также



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

