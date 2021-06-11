---
title: IProfAdminAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.AdminServices
api_type:
- COM
ms.assetid: 87235fd2-6527-41a1-98ba-b951632a1c81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c504f98655e35af62810dd428e8e04878a36dec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422084"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.
  
```cpp
HRESULT AdminServices(
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Указатель на имя измененного профиля. Параметр  _lpszProfileName_ не должен быть NULL. 
    
 _lpszPassword_
  
> [in] Всегда NULL. 
    
 _ulUIParam_
  
> [in] Ручка родительского окна для любых диалогов или окон, отображаемого этим методом.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют ирисовку объекта администрирования службы сообщений. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Включает отображение пользовательского интерфейса. 
    
MAPI_UNICODE 
  
> Имя профиля находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, имя находится в формате ANSI.
    
 _lppServiceAdmin_
  
> [вышел] Указатель на указатель на объект администрирования службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект администрирования службы сообщений был успешно возвращен.
    
MAPI_E_LOGON_FAILED 
  
> Указанный профиль не существует, или пароль был неправ, и диалоговое окно не могло отображаться пользователю, чтобы запросить правильный пароль, так как MAPI_DIALOG не был задан в  _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::AdminServices** предоставляет доступ к объекту администрирования службы сообщений для внесения изменений конфигурации в службы сообщений в профиле. 
  
 Параметр  _lpszPassword должен_ быть NULL или указатель на строку нулевой длины. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Хотя вы можете получить [указатель IMsgServiceAdmin,](imsgserviceadminiunknown.md) позвонив по этому методу или [IMAPISession::AdminServices,](imapisession-adminservices.md)позвоните **по телефону IProfAdmin::AdminServices,** если у вас строго клиент конфигурации и не предлагаются функции обмена сообщениями. **IProfAdmin::AdminServices** не создает объект сеанса и не загружает поставщиков услуг, что повышает производительность. 
  
Вы не можете использовать **IProfAdmin::AdminServices** для создания профиля. Поэтому необходимо указать существующий допустимый профиль _в lpszProfileName._ Если указанного профиля не существует, **IProfAdmin::AdminServices** возвращает MAPI_E_LOGON_FAILED. 
  
Имя профиля может быть до 64 символов в длину и может включать следующие символы:
  
- Все буквы, включая символы акцента и символы подчеркнуть. 
    
- Встроенные пробелы, но не ведущие и не ведущие.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI использует метод **IProfAdmin::AdminServices** для открытия объекта администрирования службы сообщений для выбранного профиля для добавления служб.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

