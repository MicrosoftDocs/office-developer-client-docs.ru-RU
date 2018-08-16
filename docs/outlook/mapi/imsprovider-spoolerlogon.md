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
ms.openlocfilehash: eaf84e1b2a747b313f1534eb66b190d86cf89df9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809443"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Относится к**: Outlook 
  
Журналы очереди MAPI вход в систему хранения сообщений.
  
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

## <a name="parameters"></a>Параметры

 _lpMAPISup_
  
> [in] Указатель на MAPI поддержку объектов хранилища сообщений.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод. 
    
 _lpszProfileName_
  
> [in] Указатель на строку, содержащую имя профиля, используется для входа очереди MAPI. Эта строка может отображаются в диалоговых окнах, записывается в файл журнала или просто игнорируются. Он должен быть в формате Юникод, если флаг MAPI_UNICODE установлен в параметре _ulFlags_ . 
    
 _cbEntryID_
  
> [in] Размер в байтах, идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи для хранилища сообщений. Указать значение NULL для параметра _lpEntryID_ указывает, что хранилище сообщений еще не был выбран и диалоговых окон, которые позволяют пользователю выбрать хранилище сообщений могут быть представлены. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как выполняется вход в систему. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Разрешено для успешного выполнения даже в том случае, если базовый объект недоступен для вызова реализации. Если объект недоступен, следующий вызов объекта может вызвать ошибку.
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если MAPI_UNICODE не задано, они в формате ANSI.
    
MDB_NO_DIALOG 
  
> Не отображать диалоговые окна входа в систему. Если этот флаг установлен, возвращается значение ошибка MAPI_E_LOGON_FAILED, если вход в систему не удалось. Если этот флаг не установлен, поставщик хранения сообщений можно запрашивать пользователя в нужное имя или пароль, вставьте диск или выполнить другие действия, необходимые для установления подключения к хранилищу.
    
MDB_WRITE 
  
> Запросы на разрешение чтения и записи.
    
 _lpInterface_
  
> [in] Указатель на интерфейс идентификатор (ИД интерфейса) для хранилища сообщений для входа в систему. Значение NULL указывает, что возвращается интерфейс MAPI для хранилища сообщений ([IMsgStore](imsgstoreimapiprop.md)). Параметр _lpInterface_ можно также назначается идентификатор соответствующий интерфейс для хранилища сообщений (например, IID_IUnknown или IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Указатель на размер в байтах, проверки данных с помощью параметра _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> [in] Указатель на указатель на данные проверки. Метод **SpoolerLogon** использует эти данные для входа в качестве поставщика хранилища сообщений, ранее вход в систему с помощью метода [IMSProvider::Logon](imsprovider-logon.md) диспетчер очереди MAPI на том же хранилище. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на возвращенный [MAPIERROR](mapierror.md) структуры, если они существуют, который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата. 
    
 _lppMSLogon_
  
> [out] Указатель на указатель на сообщение хранить объект входа в систему для MAPI для входа в систему.
    
 _lppMDB_
  
> [out] Указатель на указатель на сообщение хранилища объект для очереди MAPI и клиентскими приложениями для входа в систему.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_UNCONFIGURED 
  
> Профиль не содержит достаточно сведений для входа в систему для выполнения. При возвращении это значение MAPI вызывает функцию точки входа службы сообщений поставщика хранилища сообщений.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно, но поставщика хранилища сообщений имеет доступные сведения об ошибке. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md). Чтобы получить сведения об ошибке от поставщика, вызовите метод [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI вызывает метод **IMSProvider::SpoolerLogon** войти в хранилище сообщений. Диспетчер очереди MAPI следует использовать объект хранилища сообщений, возвращенный поставщиком хранилища сообщений с помощью параметра _lppMDB_ во время и после входа в систему. 
  
Для обеспечения согласованности с помощью метода [IMSProvider::Logon](imsprovider-logon.md) поставщик возвращает объект входа хранилища сообщений с помощью параметра _lppMSLogon_ . Использование объекта хранилища и объект вход в систему идентичны для входа в систему обычным хранения; Таким образом, что объекты действовать как если бы они были одного объекта, который предоставляет два из них следует однозначного соответствия между объект вход в систему и объект хранилища. Создаются два объекта вместе и освобожденное друг с другом. 
  
Поставщик хранения во внутренней сети следует пометить объект хранилища возвращенных сообщений для указания, что хранилище используется диспетчер очереди MAPI. Некоторые методы для данного объекта хранилища ведут себя иначе, не в сообщении хранилища, который на клиентские приложения. Поддержание внутренних Марка — это чаще всего инициирования поведения, характерные для очереди MAPI.
  
## <a name="see-also"></a>См. также



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
