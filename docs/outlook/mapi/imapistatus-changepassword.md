---
title: имапистатусчанжепассворд
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
  
Изменяет пароль поставщика услуг без отображения пользовательского интерфейса. Этот метод можно дополнительно поддерживать в объектах состояния, реализованных поставщиками служб.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _лполдпасс_
  
> возврата Указатель на старый пароль.
    
 _лпневпасс_
  
> возврата Указатель на новый пароль.
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют форматом паролей. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Пароли имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, пароли имеют формат ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Пароль успешно изменен.
    
MAPI_E_NO_ACCESS 
  
> Старый пароль, на который указывает _лполдпасс_ , является недопустимым. 
    
MAPI_E_NO_SUPPORT 
  
> Объект Status не поддерживает эту операцию, как указано в отсутствие флага STATUS_CHANGE_PASSWORD в свойстве **PR_RESOURCE_METHODS** объекта Status ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
## <a name="remarks"></a>Примечания

Не все объекты Status поддерживают метод **имапистатус:: ChangePassword** . Он поддерживается только поставщиками услуг, которым требуются клиенты для ввода пароля. Ни один из объектов состояния, реализуемых MAPI, не поддерживает операцию смены пароля. 
  
 **ChangePassword** изменяет пароль программным способом без взаимодействия с пользователем. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Удаленные поставщики транспорта реализуют **ChangePassword** , как указано ниже. Нет специальных рекомендаций. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

