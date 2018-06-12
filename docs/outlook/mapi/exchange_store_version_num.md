---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 00d92f8e2ec3af766d5b241d1a911be304b346d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808394"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="14a90-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="14a90-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="14a90-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="14a90-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="14a90-105">Сохранение сведений о версии для Microsoft Exchange Server, подключенные учетные записи в профиле Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="14a90-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="14a90-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="14a90-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="14a90-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="14a90-107">Members</span></span>

 <span data-ttu-id="14a90-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="14a90-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="14a90-109">Основной номер версии, который обычно увеличивается при выпуска содержит значительные новые функции и изменения в функциональных возможностях.</span><span class="sxs-lookup"><span data-stu-id="14a90-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="14a90-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="14a90-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="14a90-111">Дополнительный номер версии, который соответствует определенный основной номер версии и, как правило будет увеличен при выпуске незначительные новые функции и основные исправления.</span><span class="sxs-lookup"><span data-stu-id="14a90-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="14a90-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="14a90-112">_wBuild_</span></span>
  
- <span data-ttu-id="14a90-113">Основной номер построения, который соответствует определенного основной и дополнительный номер и, как правило будет увеличен в внутренний выпуск, который содержит новые функции или исправления.</span><span class="sxs-lookup"><span data-stu-id="14a90-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="14a90-114">Это значение также увеличивается при выпуске основных внутреннего кода филиала или вехи, такие как версия-кандидат.</span><span class="sxs-lookup"><span data-stu-id="14a90-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="14a90-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="14a90-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="14a90-116">Номер дополнительный номер сборки, обычно увеличивается в внутренний выпуск, который содержит новые функции или исправляет, соответствующие определенным основных построения, который обозначает основных кода филиала или вехи.</span><span class="sxs-lookup"><span data-stu-id="14a90-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="14a90-117">См. также</span><span class="sxs-lookup"><span data-stu-id="14a90-117">See also</span></span>



[<span data-ttu-id="14a90-118">О дополнения MAPI</span><span class="sxs-lookup"><span data-stu-id="14a90-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="14a90-119">Каноническое свойство PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="14a90-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

