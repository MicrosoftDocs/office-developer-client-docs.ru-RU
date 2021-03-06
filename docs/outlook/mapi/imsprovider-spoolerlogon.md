---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430576"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регистрирую пульпер MAPI в хранилище сообщений.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Parameters

 _lpMAPISup_
  
> [in] Указатель на объект поддержки MAPI для магазина сообщений.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом. 
    
 _lpszProfileName_
  
> [in] Указатель на строку, содержаную имя профиля, используемого для логотипа пульпера MAPI. Эта строка может отображаться в диалоговом окне, записана в файл журнала или просто игнорируется. Он должен быть в формате Unicode, если MAPI_UNICODE в параметре _ulFlags._ 
    
 _cbEntryID_
  
> [in] Размер в bytes идентификатора записи, на который указывает _параметр lpEntryID._ 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для магазина сообщений. Передача NULL в  _параметре lpEntryID_ указывает на то, что хранилище сообщений еще не выбрано и что диалоговые окна, позволяющие пользователю выбрать хранилище сообщений, могут быть представлены. 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют выполнение логотипа. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Вызов может быть успешным, даже если его объект недопустим для реализации вызова. Если объект не доступен, последующий вызов объекта может привести к ошибке.
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если MAPI_UNICODE не установлено, строки находятся в формате ANSI.
    
MDB_NO_DIALOG 
  
> Предотвращает отображение диалогов с логотипом. Если этот флаг заданной, значение MAPI_E_LOGON_FAILED возвращается, если логотип неуспешен. Если этот флаг не установлен, поставщик магазина сообщений может побудить пользователя исправить имя или пароль, вставить диск или выполнить другие действия, необходимые для установления подключения к магазину.
    
MDB_WRITE 
  
> Запросы на чтение и написание разрешений.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID) для входа в хранилище сообщений. Передача NULL указывает, что возвращается интерфейс MAPI для магазина сообщений[(IMsgStore).](imsgstoreimapiprop.md) Параметр  _lpInterface_ также может быть задан идентификатору для соответствующего интерфейса для магазина сообщений (например, IID_IUnknown или IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Указатель на размер в bytes данных проверки в _параметре lppbSpoolSecurity._ 
    
 _lpbSpoolSecurity_
  
> [in] Указатель на указатель на данные проверки. Метод **SpoolerLogon** использует эти данные для входа шпалерОВ MAPI в тот же магазин, в который ранее входил поставщик магазина сообщений с помощью метода [IMSProvider::Logon.](imsprovider-logon.md) 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращаемую структуру [MAPIERROR,](mapierror.md) если таковые есть, содержит сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError может_ быть задан в NULL, если нет структуры **MAPIERROR** для возврата. 
    
 _lppMSLogon_
  
> [вышел] Указатель на указатель на объект логотипа магазина сообщений для входа в MAPI.
    
 _lppMDB_
  
> [вышел] Указатель на указатель на объект хранения сообщений для пульпера MAPI и клиентских приложений для входа в систему.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNCONFIGURED 
  
> Профиль не содержит достаточно сведений для завершения логотипа. Когда это значение возвращается, MAPI вызывает функцию точки входа в службу входа поставщика сообщений поставщика сообщений.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался, но у поставщика магазина сообщений есть сведения об ошибках. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md) Чтобы получить сведения об ошибках от поставщика, позвоните по [методу IMAPISession::GetLastError.](imapisession-getlasterror.md) 
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IMSProvider::SpoolerLogon** для входа в хранилище сообщений. Пульпер MAPI должен использовать объект хранения сообщений, возвращенный поставщиком магазина сообщений в  _параметре lppMDB_ во время и после логотипа. 
  
Для согласованности с методом [IMSProvider::Logon](imsprovider-logon.md) поставщик также возвращает объект logon магазина сообщений в _параметре lppMSLogon._ Использование объекта магазина и объекта logon идентично обычному логотипу магазина; между объектом logon и объектом магазина должна быть одна к одной, чтобы объекты действовали так, как если бы они были одним объектом, который предоставляет два интерфейса. Эти два объекта создаются вместе и освобождены вместе. 
  
Поставщик магазина должен внутренне отметить объект возвращенного магазина сообщений, чтобы указать, что хранилище используется spooler MAPI. Некоторые методы для этого объекта магазина ведут себя иначе, чем для объекта хранения сообщений, предоставляемого для клиентских приложений. Сохранение этой внутренней метки является наиболее распространенным способом запуска поведения, определенного для пулера MAPI.
  
## <a name="see-also"></a>См. также



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

