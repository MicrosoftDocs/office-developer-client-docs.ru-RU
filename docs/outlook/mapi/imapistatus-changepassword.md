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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Изменяет пароль поставщика услуг без отображения пользовательского интерфейса. Этот метод необязательно поддерживается в объектах состояния, которые реализуют поставщики услуг.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpOldPass_
  
> [in] Указатель на старый пароль.
    
 _lpNewPass_
  
> [in] Указатель на новый пароль.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют формат паролей. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Пароли находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, пароли находятся в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Изменение пароля было успешным.
    
MAPI_E_NO_ACCESS 
  
> Старый пароль, на который указывает  _lpOldPass,_ недействителен. 
    
MAPI_E_NO_SUPPORT 
  
> Объект состояния не поддерживает эту операцию, о чем свидетельствует отсутствие флага STATUS_CHANGE_PASSWORD в свойстве PR_RESOURCE_METHODS объекта **состояния** [(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Не все объекты состояния поддерживают **метод IMAPIStatus::ChangePassword.** Он поддерживается только поставщиками услуг, которые требуют от клиентов ввести пароль. Ни один из объектов состояния, которые реализует MAPI, не поддерживает операцию изменения пароля. 
  
 **ChangePassword** изменяет пароль программным путем, без взаимодействия с пользователем. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Удаленные поставщики транспорта **реализуют ChangePassword,** как указано здесь. Особых соображений нет. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

