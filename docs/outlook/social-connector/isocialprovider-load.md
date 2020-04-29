---
title: исоЦиалпровидерлоад
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Инициализирует поставщик Outlook Social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285762"
---
# <a name="isocialproviderload"></a><span data-ttu-id="362ff-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="362ff-103">ISocialProvider::Load</span></span>

<span data-ttu-id="362ff-104">Инициализирует поставщик Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="362ff-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="362ff-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="362ff-105">Parameters</span></span>

<span data-ttu-id="362ff-106">_соЦиалпровидеринтерфацеверсион_</span><span class="sxs-lookup"><span data-stu-id="362ff-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="362ff-107">возврата Версия интерфейсов поставщика OSC, ожидаемых для OSC.</span><span class="sxs-lookup"><span data-stu-id="362ff-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="362ff-108">_лангуажетаг_</span><span class="sxs-lookup"><span data-stu-id="362ff-108">_languageTag_</span></span>
  
> <span data-ttu-id="362ff-109">возврата Тег языка IETF, определяемый [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) и [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), который представляет текущий язык пользовательского интерфейса Outlook.</span><span class="sxs-lookup"><span data-stu-id="362ff-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="362ff-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="362ff-110">Remarks</span></span>

<span data-ttu-id="362ff-111">Формат версии для параметра _соЦиалпровидеринтерфацеверсион_ — _X_. _XXXX_, где _X_ — это основная версия, а _XXXX_ — вспомогательная версия OSC.</span><span class="sxs-lookup"><span data-stu-id="362ff-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="362ff-112">Для Office 2013 проверьте наличие основной версии 15.</span><span class="sxs-lookup"><span data-stu-id="362ff-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="362ff-113">См. также</span><span class="sxs-lookup"><span data-stu-id="362ff-113">See also</span></span>

- [<span data-ttu-id="362ff-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="362ff-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

