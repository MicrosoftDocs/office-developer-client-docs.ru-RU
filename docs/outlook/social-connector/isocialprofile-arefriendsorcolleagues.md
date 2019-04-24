---
title: ИсоЦиалпрофилеарефриендсорколлеагуес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Определяет, являются ли указанные пользователи друзьями.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331670"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Определяет, являются ли указанные пользователи друзьями.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Параметры

_userIds_
  
> возврата Структура, указывающая массив значений идентификатора пользователя, соответствующих набору людей в социальной сети.
    
_результатом_
  
> вышли Указатель на структуру, задающую массив логических значений, указывающий, является ли соответствующий пользователь в массиве _UserID_ дружественным. 
    
## <a name="remarks"></a>Комментарии

Для каждого пользователя, представленного в массиве входных данных параметра _UserID_ , этот метод задает соответствующий элемент в выходном массиве параметра _Results_ . **значение true** указывает, что пользователь является дружественным, а **значение false** указывает, что пользователь не является дружественным. 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

