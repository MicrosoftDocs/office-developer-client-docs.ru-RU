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
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="b2a8d-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="b2a8d-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="b2a8d-104">Определяет, будет ли указанных пользователей друзей.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="b2a8d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2a8d-105">Parameters</span></span>

<span data-ttu-id="b2a8d-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="b2a8d-106">_userIds_</span></span>
  
> <span data-ttu-id="b2a8d-107">[in] Структура, которая указывает массив значений Идентификаторов пользователей, которые соответствуют набору лиц в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="b2a8d-108">_результаты_</span><span class="sxs-lookup"><span data-stu-id="b2a8d-108">_results_</span></span>
  
> <span data-ttu-id="b2a8d-109">[out] Указатель на структуру, которая указывает массив значений типа Boolean, указывающее, является ли соответствующий человека в массиве _userIds_ друг.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2a8d-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2a8d-110">Remarks</span></span>

<span data-ttu-id="b2a8d-111">Для каждого пользователя, представленных в массиве входного параметра _userIds_ этого метода можно задать соответствующих элементов в массиве вывода _результатов_ для параметра.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="b2a8d-112">**значение true,** указывает, что сотрудник, друзей и **значение false** указывает, что пользователь не друга.</span><span class="sxs-lookup"><span data-stu-id="b2a8d-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b2a8d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="b2a8d-113">See also</span></span>

- [<span data-ttu-id="b2a8d-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="b2a8d-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

