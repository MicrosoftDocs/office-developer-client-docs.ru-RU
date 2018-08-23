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
ms.openlocfilehash: a9e596ff8561d5aabc71ffe3540efaeef8f5b83d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593986"
---
# <a name="iprofadminadminservices"></a>IProfAdmin::AdminServices

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указатель на имя профиля, который нужно изменить. Параметр _lpszProfileName_ не должна быть NULL. 
    
 _lpszPassword_
  
> [in] Всегда имеет значение NULL. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна для любого диалоговые окна или окна, которые отображаются этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет извлечения объект администрирования службы сообщений. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Включение отображения пользовательского интерфейса. 
    
MAPI_UNICODE 
  
> Имя профиля — в формате Юникод. Если флаг MAPI_UNICODE не установлен, — это имя в формате ANSI.
    
 _lppServiceAdmin_
  
> [out] Указатель на указатель на объект администрирования службы сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Объект администрирования службы сообщение успешно возвращен.
    
MAPI_E_LOGON_FAILED 
  
> Указанный профиль не существует, или пароль был неверный и диалоговое окно "" не удается отобразить для пользователя, чтобы запросить правильный пароль, так как MAPI_DIALOG не установлен в _ulFlags_.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::AdminServices** предоставляет доступ к объекту администрирования службы сообщений для изменения конфигурации службы сообщений в профиле. 
  
 Параметр _lpszPassword_ должен быть NULL или указатель на строку нулевой длины. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несмотря на то, что указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) можно получить путем вызова метода или в этом [IMAPISession::AdminServices](imapisession-adminservices.md), вызовите **IProfAdmin::AdminServices** , если у пользователя имеется строго конфигурации клиента и предлагают нет функции обмена сообщениями. **IProfAdmin::AdminServices** не создается объект сеанса и не загружать никаких поставщиков услуг которого повышает производительность. 
  
**IProfAdmin::AdminServices** нельзя использовать для создания профиля. Таким образом необходимо указать допустимое существующего профиля в _lpszProfileName_. Если указанный профиль не существует, **IProfAdmin::AdminServices** возвращает MAPI_E_LOGON_FAILED. 
  
Имя профиля может быть длиной до 64 символов и может содержать следующие символы:
  
- Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания. 
    
- Пробелы, но не начальных и конечных пробелов.
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> | HrAddServiceToProfile  <br/> |Mfcmapi (en) использует метод **IProfAdmin::AdminServices** для открытия объект сообщения службы администрирования для выбранного профиля для добавления служб.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::AdminServices](imapisession-adminservices.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

