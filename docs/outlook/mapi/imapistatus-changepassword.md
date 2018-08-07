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
ms.openlocfilehash: b667f56553b717f1bc938b6ce045dbfdde8fdc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809093"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Относится к**: Outlook 
  
Изменение пароля поставщика услуг без отображения пользовательского интерфейса. Этот метод при необходимости поддерживается в состоянии объекты, которые реализуют поставщиков услуг.
  
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
  
> [in] Битовая маска флаги, который определяет формат паролей. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Пароли, в формате Юникод. Если флаг MAPI_UNICODE не установлен, пароли, в формате ANSI.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Изменение пароля прошла успешно.
    
MAPI_E_NO_ACCESS 
  
> Старый пароль, на который указывает _lpOldPass_ является недопустимым. 
    
MAPI_E_NO_SUPPORT 
  
> Состояние объект не поддерживает эту операцию, как указано в отсутствие флага STATUS_CHANGE_PASSWORD в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) состояние объекта.
    
## <a name="remarks"></a>Замечания

Не все объекты состояния поддерживают метод **IMAPIStatus::ChangePassword** . Поддерживается только поставщиков услуг, клиентам необходимо ввести пароль. Ни один из состояния объекты, внедряемые MAPI не поддерживает операцию смены пароля. 
  
 **Изменение пароля** программным способом, изменяет пароль без взаимодействия с пользователем. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщики удаленного транспорта реализовать **Изменение пароля** , указанный здесь. Существует не особенности. 
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

