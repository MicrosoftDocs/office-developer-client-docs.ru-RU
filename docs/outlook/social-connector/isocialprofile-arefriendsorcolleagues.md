---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Определяет, будет ли указанных пользователей друзей.
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812722"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Определяет, будет ли указанных пользователей друзей.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Параметры

_userIds_
  
> [in] Структура, которая указывает массив значений Идентификаторов пользователей, которые соответствуют набору лиц в социальных сетях.
    
_результаты_
  
> [out] Указатель на структуру, которая указывает массив значений типа Boolean, указывающее, является ли соответствующий человека в массиве _userIds_ друг. 
    
## <a name="remarks"></a>Замечания

Для каждого пользователя, представленных в массиве входного параметра _userIds_ этого метода можно задать соответствующих элементов в массиве вывода _результатов_ для параметра. **значение true,** указывает, что сотрудник, друзей и **значение false** указывает, что пользователь не друга. 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

