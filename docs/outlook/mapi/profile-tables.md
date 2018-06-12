---
title: Профиль таблиц
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812063"
---
# <a name="profile-tables"></a><span data-ttu-id="a0420-103">Профиль таблиц</span><span class="sxs-lookup"><span data-stu-id="a0420-103">Profile Tables</span></span>

  
  
<span data-ttu-id="a0420-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0420-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0420-105">В таблице профилей приведены сведения о всех профилей, связанных с определенной клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="a0420-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="a0420-106">Существует одна таблица профиль для каждого сеанса реализован MAPI для использования клиентами.</span><span class="sxs-lookup"><span data-stu-id="a0420-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="a0420-107">Для доступа клиентов к таблице профилей путем вызова метода [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="a0420-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="a0420-108">В таблице профилей — это статическая таблица.</span><span class="sxs-lookup"><span data-stu-id="a0420-108">The profile table is a static table.</span></span> <span data-ttu-id="a0420-109">Профили, помеченные для удаления не включаются в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="a0420-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="a0420-110">Как большинство реализаций таблицы, если называется **GetProfileTable** и нет профилей, доступных для клиента, создается таблица с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="a0420-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="a0420-111">Следующие свойства составляют обязательный столбец, задайте в таблицах профилей:</span><span class="sxs-lookup"><span data-stu-id="a0420-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="a0420-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a0420-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="a0420-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a0420-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0420-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a0420-114">See also</span></span>



[<span data-ttu-id="a0420-115">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="a0420-115">MAPI Tables</span></span>](mapi-tables.md)

