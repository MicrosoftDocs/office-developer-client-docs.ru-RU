---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410359"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Изменяет пароль поставщика услуг без отображения пользовательского интерфейса. При желании этот метод поддерживается в объектах состояния, реализуемых поставщиками служб.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpOldPass_
  
> [in] Указатель на старый пароль.
    
 _lpNewPass_
  
> [in] Указатель на новый пароль.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет форматом паролей. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Пароли имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, пароли имеют формат ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Изменение пароля было успешным.
    
MAPI_E_NO_ACCESS 
  
> Старый пароль, на который указывает  _lpOldPass,_ недействителен. 
    
MAPI_E_NO_SUPPORT 
  
> Объект состояния не поддерживает эту операцию, на что указывает отсутствие флага STATUS_CHANGE_PASSWORD в свойстве **PR_RESOURCE_METHODS** объекта status [(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Не все объекты состояния поддерживают метод **IMAPIStatus::ChangePassword.** Она поддерживается только поставщиками услуг, которые требуют ввода пароля клиентами. Ни один из объектов состояния, реализуемого MAPI, не поддерживает операцию смены пароля. 
  
 **ChangePassword** изменяет пароль программным путем без участия пользователя. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики удаленных транспортных услуг **реализуют ChangePassword,** как указано здесь. Нет особых соображений. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

