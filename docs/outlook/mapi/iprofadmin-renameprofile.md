---
title: ипрофадминренамепрофиле
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419522"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Назначает новое имя профилю.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _лпсзолдпрофиленаме_
  
> возврата Указатель на текущее имя профиля, которое требуется переименовать.
    
 _лпсзолдпассворд_
  
> возврата Всегда имеет значение NULL.
    
 _лпсзневпрофиленаме_
  
> возврата Указатель на новое имя профиля, который требуется переименовать.
    
 _улуипарам_
  
> возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом. 
    
 _ulFlags_
  
> возврата Всегда имеет значение NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль успешно переименован.
    
MAPI_E_LOGON_FAILED 
  
> Недопустимый пароль профиля.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **ипрофадмин:: ренамепрофиле** назначает новое имя профилю, если он имеет такой профиль. Если профиль для переименования используется клиентом при вызове **ренамепрофиле** , **ренамепрофиле** помечает профиль и возвращает S_OK вместо того, чтобы выполнять операцию переименования во время использования профиля. Если профиль больше не используется, **ренамепрофиле** назначает ему новое имя. 
  
Длина старого и нового имен профиля может доставлять до 64 символов и содержать следующие символы:
  
- Все буквенно-цифровые символы, включая диакритические знаки и символ подчеркивания.
    
- Внутренние пробелы, но не ведущие и замыкающие пробелы.
    
_Лпсзпассворд_ всегда должно иметь значение null или быть указателем на строку нулевой длины. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

