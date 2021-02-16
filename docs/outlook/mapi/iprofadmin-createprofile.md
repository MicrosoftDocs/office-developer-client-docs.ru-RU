---
title: IProfAdminCreateProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CreateProfile
api_type:
- COM
ms.assetid: 10cda14a-8f93-41e0-b1fb-500098bdc392
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b104c62eb617e6c68f85dea4ef6379c831733844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404402"
---
# <a name="iprofadmincreateprofile"></a>IProfAdmin::CreateProfile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает новый профиль.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя нового профиля.
    
 _lpszPassword_
  
> [in] Указатель на пароль нового профиля. 
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет процессом создания профиля. Можно установить следующие флаги:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI должен заполнить новый профиль службами сообщений, включенными в раздел [Службы по умолчанию] файла Mapisvc.inf.
    
MAPI_DIALOG 
  
> Можно отобразить таблицы свойств конфигурации каждого из поставщиков добавляемой службы сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Создан новый профиль.
    
MAPI_E_NO_ACCESS 
  
> Указанный новый профиль уже существует.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::CreateProfile** создает новый профиль. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно вызвать **CreateProfile** во время установки приложения или в любое время во время сеанса. Когда этот метод вызван во время установки, многие параметры конфигурации приходят из файла конфигурации Mapisvc.inf. Когда этот метод вызван во время активного сеанса, параметры приходят от пользователя, который получает запрос через ряд листов свойств. 
  
Если флаг MAPI_DEFAULT_SERVICES установлен в параметре  _ulFlags,_ **CreateProfile** вызывает функцию точки входа службы сообщений для каждой службы сообщений в разделе [Службы по умолчанию] в файле Mapisvc.inf. Каждая функция точки входа службы сообщений вызвана с параметром  _ulContext,_ для MSG_SERVICE_CREATE. 
  
Если установлены MAPI_DIALOG и MAPI_DEFAULT_SERVICES, значения  _параметров ulUIParam_ и  _ulFlags_ также передаются функции точки входа службы сообщений. Функции точки входа службы сообщений будут вызваны только после того, как все доступные сведения из файла Mapisvc.inf будут добавлены в профиль. 
  
Имя нового профиля и его пароль могут быть длиной до 64 символов и могут включать следующие символы:
  
- Все буквы и цифры, включая знаки акцента и символ подчеркиваения.
    
- Внедренные пробелы, но не пробелы в первой или вехе.
    
Параметр  _lpszPassword должен_ иметь значение NULL или указатель на строку нулевой длины. 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

