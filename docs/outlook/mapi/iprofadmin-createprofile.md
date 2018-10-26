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
ms.openlocfilehash: 92d5dcdf3e5e3fbdb7490d777a24976c9ae4af1a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582793"
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

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя нового профиля.
    
 _lpszPassword_
  
> [in] Указатель на пароль нового профиля. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ создания профилей. Можно задать следующие флажки:
    
MAPI_DEFAULT_SERVICES 
  
> MAPI должен заполнить новый профиль с помощью службы сообщений, которые включены в разделе [службы по умолчанию] файла Mapisvc.inf.
    
MAPI_DIALOG 
  
> Отображения свойств конфигурации всех поставщиков в службах сообщение будет добавлена. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Был создан новый профиль.
    
MAPI_E_NO_ACCESS 
  
> Указанный новый профиль уже существует.
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::CreateProfile** создает новый профиль. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно вызвать **CreateProfile** во время установки приложения или в любой момент во время сеанса. Когда этот метод вызывается во время установки, многие из параметров конфигурации поступают из конфигурации файла Mapisvc.inf. Когда этот метод вызывается во время активного сеанса, параметры поступают от пользователя, который будет запрашиваться ряд свойств. 
  
Если в параметре _ulFlags_ флаг MAPI_DEFAULT_SERVICES, **CreateProfile** вызывает функцию точки входа службы сообщений для каждой службы сообщений в разделе [службы по умолчанию] в файле Mapisvc.inf. Каждой функции точки входа службы сообщений вызывается с параметром _ulContext_ установлено значение MSG_SERVICE_CREATE. 
  
Если установлены флаги MAPI_DIALOG и MAPI_DEFAULT_SERVICES, значения в параметрах _ulUIParam_ и _ulFlags_ также передаются в функцию точки входа службы сообщений. Функции точка входа службы сообщений, называются только после все доступные сведения из файла Mapisvc.inf был добавлен к профилю. 
  
Имя нового профиля и его пароль может быть длиной до 64 символов и может содержать следующие символы:
  
- Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.
    
- Пробелы, но не начальных и конечных пробелов.
    
Параметр _lpszPassword_ должен быть NULL или указатель на строку нулевой длины. 
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

