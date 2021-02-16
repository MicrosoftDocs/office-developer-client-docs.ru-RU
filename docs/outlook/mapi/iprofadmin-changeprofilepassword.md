---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420243"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Устарело. Изменяет пароль для профиля.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя профиля, связанного с паролем, который необходимо изменить.
    
 _lpszOldPassword_
  
> [in] Указатель на текущий пароль.
    
 _lpszNewPassword_
  
> [in] Указатель на новый пароль.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом переданных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля и пароли имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Если этот метод вызван, он возвращает S_OK. Однако никаких действий не будет.
    
## <a name="remarks"></a>Примечания

Не используйте этот метод. MAPI не поддерживает пароли для профилей.
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

