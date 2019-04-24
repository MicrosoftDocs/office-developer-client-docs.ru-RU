---
title: ИсоЦиалсессионфиндперсон
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285373"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="25eea-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="25eea-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="25eea-104">Получает строку, представляющую одного или нескольких лиц, которые совпадают с параметром _UserID_ .</span><span class="sxs-lookup"><span data-stu-id="25eea-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="25eea-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="25eea-105">Parameters</span></span>

<span data-ttu-id="25eea-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="25eea-106">_userId_</span></span>
  
> <span data-ttu-id="25eea-107">возврата Идентификатор пользователя социальной сети, SMTP-адрес или отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="25eea-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="25eea-108">_result_</span><span class="sxs-lookup"><span data-stu-id="25eea-108">_result_</span></span>
  
> <span data-ttu-id="25eea-109">вышли XML-строка, представляющая одного или нескольких лиц, которые совпадают с идентификационными данными, указанными в параметре _UserID_ .</span><span class="sxs-lookup"><span data-stu-id="25eea-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="25eea-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="25eea-110">Remarks</span></span>

<span data-ttu-id="25eea-111">Если один или несколько пользователей соответствуют запросу **финдперсон** , этот метод возвращает сведения об этих лицах в параметре _result_ .</span><span class="sxs-lookup"><span data-stu-id="25eea-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="25eea-112">_Результирующая_ XML-строка должна соответствовать определению схемы для **друзей**, как определено в схеме Расширяемость поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="25eea-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="25eea-113">См. также</span><span class="sxs-lookup"><span data-stu-id="25eea-113">See also</span></span>

- [<span data-ttu-id="25eea-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="25eea-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

