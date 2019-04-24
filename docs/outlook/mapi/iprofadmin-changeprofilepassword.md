---
title: Ипрофадминчанжепрофилепассворд
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317124"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устаревшие. Изменяет пароль для профиля.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _Лпсзпрофиленаме_
  
> возврата Указатель на имя профиля, связанного с изменяемым паролем.
    
 _Лпсзолдпассворд_
  
> возврата Указатель на текущий пароль.
    
 _Лпсзневпассворд_
  
> возврата Указатель на новый пароль.
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют типом переданных строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля и пароль имеют формат Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, эти строки представлены в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> При вызове этого метода он возвратит значение S_OK. Однако никакие действия не выполняются.
    
## <a name="remarks"></a>Замечания

Не используйте этот метод. MAPI не поддерживает пароли для профилей.
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

