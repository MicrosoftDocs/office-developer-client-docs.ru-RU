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
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433726"
---
# <a name="exchange_store_version_num"></a><span data-ttu-id="cdbc6-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="cdbc6-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="cdbc6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdbc6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdbc6-105">Хранит сведения о версии для сервера Microsoft Exchange, к которому подключены учетные записи в профиле Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cdbc6-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="cdbc6-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="cdbc6-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="cdbc6-107">Members</span></span>

 <span data-ttu-id="cdbc6-108">_вмажорверсион_</span><span class="sxs-lookup"><span data-stu-id="cdbc6-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="cdbc6-109">Основной номер версии, который обычно увеличивается, когда выпуск содержит существенные новые функции и изменения в функциональных возможностях.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="cdbc6-110">_вминорверсион_</span><span class="sxs-lookup"><span data-stu-id="cdbc6-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="cdbc6-111">Дополнительный номер версии, соответствующий определенному основному номеру версии, который обычно увеличивается, если выпуск содержит незначительные новые функции или существенные исправления.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="cdbc6-112">_вбуилд_</span><span class="sxs-lookup"><span data-stu-id="cdbc6-112">_wBuild_</span></span>
  
- <span data-ttu-id="cdbc6-113">Основной номер сборки, соответствующий определенным основным и дополнительным номерам версий, который обычно увеличивается во внутреннем выпуске, содержащем новые функции или исправления.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="cdbc6-114">Это значение также увеличивается, когда выпуск является основной внутренней ветвью кода или вехой, например версией-кандидатом.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="cdbc6-115">_вминорбуилд_</span><span class="sxs-lookup"><span data-stu-id="cdbc6-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="cdbc6-116">Дополнительный номер сборки, который обычно увеличивается во внутреннем выпуске, в котором содержатся новые функции или исправления, соответствующие определенному основному построению, которое обозначает основную ветвь кода или веху.</span><span class="sxs-lookup"><span data-stu-id="cdbc6-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdbc6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cdbc6-117">See also</span></span>



[<span data-ttu-id="cdbc6-118">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="cdbc6-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="cdbc6-119">Каноническое свойство PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="cdbc6-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

