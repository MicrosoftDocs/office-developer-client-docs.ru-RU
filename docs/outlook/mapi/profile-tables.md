---
title: Таблицы профилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571481"
---
# <a name="profile-tables"></a><span data-ttu-id="3c408-103">Таблицы профилей</span><span class="sxs-lookup"><span data-stu-id="3c408-103">Profile Tables</span></span>

  
  
<span data-ttu-id="3c408-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c408-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c408-105">В таблице профилей приведены сведения о всех профилей, связанных с определенной клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="3c408-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="3c408-106">Существует одна таблица профиль для каждого сеанса реализован MAPI для использования клиентами.</span><span class="sxs-lookup"><span data-stu-id="3c408-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="3c408-107">Для доступа клиентов к таблице профилей путем вызова метода [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="3c408-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="3c408-108">В таблице профилей — это статическая таблица.</span><span class="sxs-lookup"><span data-stu-id="3c408-108">The profile table is a static table.</span></span> <span data-ttu-id="3c408-109">Профили, помеченные для удаления не включаются в таблице профилей.</span><span class="sxs-lookup"><span data-stu-id="3c408-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="3c408-110">Как большинство реализаций таблицы, если называется **GetProfileTable** и нет профилей, доступных для клиента, создается таблица с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="3c408-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="3c408-111">Следующие свойства составляют обязательный столбец, задайте в таблицах профилей:</span><span class="sxs-lookup"><span data-stu-id="3c408-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="3c408-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3c408-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="3c408-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3c408-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c408-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3c408-114">See also</span></span>



[<span data-ttu-id="3c408-115">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="3c408-115">MAPI Tables</span></span>](mapi-tables.md)

