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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя профиля, который необходимо изменить. Параметр  _lpszProfileName не_ должен иметь NULL. 
    
 _lpszPassword_
  
> [in] Всегда NULL. 
    
 _ulUIParam_
  
> [in] Handle of the parent window for any dialog boxes or windows that this method displays.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет искомым объектом администрирования службы сообщений. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Включает отображение пользовательского интерфейса. 
    
MAPI_UNICODE 
  
> Имя профиля имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, имя будет в формате ANSI.
    
 _lppServiceAdmin_
  
> [out] Указатель на указатель на объект администрирования службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект администрирования службы сообщений успешно возвращен.
    
MAPI_E_LOGON_FAILED 
  
> Указанный профиль не существует или пароль был неправильным, и пользователю не удалось отобразить диалоговое окно для запроса правильного пароля, так как MAPI_DIALOG не задан в _ulFlags._
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::AdminServices** предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в конфигурацию служб сообщений в профиле. 
  
 Параметр  _lpszPassword должен_ иметь значение NULL или указатель на строку нулевой длины. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Хотя вы можете получить указатель [IMsgServiceAdmin,](imsgserviceadminiunknown.md) вызовите этот метод или [IMAPISession::AdminServices](imapisession-adminservices.md), вызовите **IProfAdmin::AdminServices,** если у вас есть строго клиент конфигурации и не предлагаются функции обмена сообщениями. **IProfAdmin::AdminServices** не создает объект сеанса и не загружает поставщиков услуг, что повышает производительность. 
  
Для создания профиля нельзя использовать **IProfAdmin::AdminServices.** Поэтому необходимо указать существующий действительный профиль _в lpszProfileName._ Если указанный профиль не существует, **IProfAdmin::AdminServices** возвращает MAPI_E_LOGON_FAILED. 
  
Длина имени профиля может быть не более 64 символов и включать следующие символы:
  
- Все буквы и цифры, включая знаки акцента и символ подчеркиваения. 
    
- Внедренные пробелы, но не пробелы в первой или вехе.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |MFCMAPI использует метод **IProfAdmin::AdminServices,** чтобы открыть объект администрирования службы сообщений для выбранного профиля для добавления служб.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

