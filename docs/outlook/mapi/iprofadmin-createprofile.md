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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает новый профиль.
  
```cpp
HRESULT CreateProfile(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Указатель на имя нового профиля.
    
 _lpszPassword_
  
> [in] Указатель на пароль нового профиля. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.
    
 _ulFlags_
  
> [in] Битмаски флагов, которые контролируют, как создается профиль. Можно установить следующие флаги:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI должна заполнить новый профиль службами сообщений, включенными в раздел [Службы по умолчанию] файла Mapisvc.inf.
    
MAPI_DIALOG 
  
> Можно отобразить листы свойств конфигурации каждого из поставщиков в добавленных службах сообщений. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Был создан новый профиль.
    
MAPI_E_NO_ACCESS 
  
> Указанный новый профиль уже существует.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::CreateProfile** создает новый профиль. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете вызвать **CreateProfile** во время установки приложения или в любое время во время сеанса. Когда этот метод вызван во время установки, многие параметры конфигурации приходят из файла конфигурации Mapisvc.inf. Когда этот метод вызван во время активного сеанса, параметры приходят от пользователя, которому подсказывался ряд листов свойств. 
  
Если флаг MAPI_DEFAULT_SERVICES установлен в параметре  _ulFlags,_ **CreateProfile** вызывает функцию точки входа службы сообщений для каждой службы сообщений в разделе [Службы по умолчанию] в файле Mapisvc.inf. Каждая функция точки входа службы сообщений называется с параметром  _ulContext,_ заданным MSG_SERVICE_CREATE. 
  
Если заданы MAPI_DIALOG и MAPI_DEFAULT_SERVICES флаги, значения  _ulUIParam_ и  _ulFlags_ также передаются функции точки входа службы сообщений. Функции точки входа службы сообщений называются только после того, как в профиль будут добавлены все доступные сведения из файла Mapisvc.inf. 
  
Имя нового профиля и его пароль могут иметь длину до 64 символов и включать следующие символы:
  
- Все буквы, включая символы акцента и символы подчеркнуть.
    
- Встроенные пробелы, но не ведущие и не ведущие.
    
Параметр  _lpszPassword должен_ быть NULL или указатель на строку нулевой длины. 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

