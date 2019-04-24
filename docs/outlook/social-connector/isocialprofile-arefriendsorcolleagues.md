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
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="2cc10-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="2cc10-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="2cc10-104">Определяет, являются ли указанные пользователи друзьями.</span><span class="sxs-lookup"><span data-stu-id="2cc10-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="2cc10-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="2cc10-105">Parameters</span></span>

<span data-ttu-id="2cc10-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="2cc10-106">_userIds_</span></span>
  
> <span data-ttu-id="2cc10-107">возврата Структура, указывающая массив значений идентификатора пользователя, соответствующих набору людей в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="2cc10-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="2cc10-108">_результатом_</span><span class="sxs-lookup"><span data-stu-id="2cc10-108">_results_</span></span>
  
> <span data-ttu-id="2cc10-109">вышли Указатель на структуру, задающую массив логических значений, указывающий, является ли соответствующий пользователь в массиве _UserID_ дружественным.</span><span class="sxs-lookup"><span data-stu-id="2cc10-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2cc10-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cc10-110">Remarks</span></span>

<span data-ttu-id="2cc10-111">Для каждого пользователя, представленного в массиве входных данных параметра _UserID_ , этот метод задает соответствующий элемент в выходном массиве параметра _Results_ .</span><span class="sxs-lookup"><span data-stu-id="2cc10-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="2cc10-112">**значение true** указывает, что пользователь является дружественным, а **значение false** указывает, что пользователь не является дружественным.</span><span class="sxs-lookup"><span data-stu-id="2cc10-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2cc10-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2cc10-113">See also</span></span>

- [<span data-ttu-id="2cc10-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="2cc10-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

