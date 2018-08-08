---
title: IProfAdminRenameProfile
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
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809510"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Относится к**: Outlook 
  
Назначает новое имя профиля.
  
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

 _lpszOldProfileName_
  
> [in] Указатель на имя текущего профиля, который требуется переименовать.
    
 _lpszOldPassword_
  
> [in] Всегда имеет значение NULL.
    
 _lpszNewProfileName_
  
> [in] Указатель на новое имя профиля, который требуется переименовать.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод. 
    
 _ulFlags_
  
> [in] Всегда имеет значение NULL.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Профиль успешно переименован.
    
MAPI_E_LOGON_FAILED 
  
> Неправильный пароль профиля.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::RenameProfile** назначается новое имя профиля, если таковой имеется. Если профиль, чтобы переименовать используется клиентом при вызове **RenameProfile** , **RenameProfile** помечает профиля и возвращает значение S_OK вместо попытки подключения операция переименования профиля во время работы. Если профиль больше не используется, **RenameProfile** назначает ее новое имя. 
  
Имена старый и новый профиль может иметь длину до 64 символов и может содержать следующие символы:
  
- Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.
    
- Пробелы, но не начальных и конечных пробелов.
    
_LpszPassword_ всегда должно быть NULL или указатель на строку нулевой длины. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

