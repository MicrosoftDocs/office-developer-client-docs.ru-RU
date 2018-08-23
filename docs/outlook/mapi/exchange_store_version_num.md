---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594476"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="bbf9b-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="bbf9b-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="bbf9b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbf9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbf9b-105">Сохранение сведений о версии для Microsoft Exchange Server, подключенные учетные записи в профиле Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bbf9b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bbf9b-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="bbf9b-107">Members</span><span class="sxs-lookup"><span data-stu-id="bbf9b-107">Members</span></span>

 <span data-ttu-id="bbf9b-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="bbf9b-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="bbf9b-109">Основной номер версии, который обычно увеличивается при выпуска содержит значительные новые функции и изменения в функциональных возможностях.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="bbf9b-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="bbf9b-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="bbf9b-111">Дополнительный номер версии, который соответствует определенный основной номер версии и, как правило будет увеличен при выпуске незначительные новые функции и основные исправления.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="bbf9b-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="bbf9b-112">_wBuild_</span></span>
  
- <span data-ttu-id="bbf9b-113">Основной номер построения, который соответствует определенного основной и дополнительный номер и, как правило будет увеличен в внутренний выпуск, который содержит новые функции или исправления.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="bbf9b-114">Это значение также увеличивается при выпуске основных внутреннего кода филиала или вехи, такие как версия-кандидат.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="bbf9b-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="bbf9b-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="bbf9b-116">Номер дополнительный номер сборки, обычно увеличивается в внутренний выпуск, который содержит новые функции или исправляет, соответствующие определенным основных построения, который обозначает основных кода филиала или вехи.</span><span class="sxs-lookup"><span data-stu-id="bbf9b-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbf9b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="bbf9b-117">See also</span></span>



[<span data-ttu-id="bbf9b-118">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="bbf9b-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="bbf9b-119">Каноническое свойство PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="bbf9b-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

