---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Определяет, являются ли указанные пользователи друзьями.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412564"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Определяет, являются ли указанные пользователи друзьями.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parameters

_userIds_
  
> [in] Структура, которая указывает массив значений пользовательского ID, соответствующих набору лиц в социальной сети.
    
_результаты_
  
> [вышел] Указатель на структуру, указывающая массив значений Boolean, указывающий, является ли соответствующий пользователь в массиве  _userIds_ другом. 
    
## <a name="remarks"></a>Примечания

Для каждого пользователя, представленного в массиве ввода _параметра userIds,_ этот метод  задает соответствующий элемент в массиве результатов. **true** указывает, что человек является  другом, а ложный указывает, что он не является другом. 
  
## <a name="see-also"></a>См. также

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

