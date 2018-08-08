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
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809515"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Относится к**: Outlook 
  
Рекомендуется использовать. Изменение пароля для профиля.
  
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
  
> [in] Указатель на имя профиля, связанные с использованием пароля, который нужно изменить.
    
 _lpszOldPassword_
  
> [in] Указатель на текущий пароль.
    
 _lpszNewPassword_
  
> [in] Указатель на новый пароль.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип строк, переданное. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля и пароли, в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Если этот метод вызывается, она возвращает значение S_OK. Тем не менее не действие не выполняется.
    
## <a name="remarks"></a>Замечания

Не используйте этот метод. MAPI не поддерживает пароли для профилей.
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

