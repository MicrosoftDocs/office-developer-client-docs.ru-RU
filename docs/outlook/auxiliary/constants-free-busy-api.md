---
title: Константы (занятости API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: В этом разделе содержатся определения констант, класс идентификаторы и идентификаторы интерфейса для API свободен/занят.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807686"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="650eb-103">Константы (занятости API)</span><span class="sxs-lookup"><span data-stu-id="650eb-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="650eb-104">В этом разделе содержатся определения констант, класс идентификаторы и идентификаторы интерфейса для API свободен/занят.</span><span class="sxs-lookup"><span data-stu-id="650eb-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="650eb-105">Константы</span><span class="sxs-lookup"><span data-stu-id="650eb-105">Constants</span></span>

|<span data-ttu-id="650eb-106">**Constant**</span><span class="sxs-lookup"><span data-stu-id="650eb-106">**Constant**</span></span>|<span data-ttu-id="650eb-107">**Определение**</span><span class="sxs-lookup"><span data-stu-id="650eb-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="650eb-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="650eb-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="650eb-109">*Определенные в файле winerror.h файл заголовка Microsoft Windows Software Development Kit (SDK).*</span><span class="sxs-lookup"><span data-stu-id="650eb-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="650eb-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="650eb-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="650eb-111">*Определенные в файле winerror.h файл заголовка пакета SDK Windows.*</span><span class="sxs-lookup"><span data-stu-id="650eb-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="650eb-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="650eb-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="650eb-113">*Определенные в файле winerror.h файл заголовка пакета SDK Windows.*</span><span class="sxs-lookup"><span data-stu-id="650eb-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="650eb-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="650eb-114">S_OK</span></span>  <br/> | <span data-ttu-id="650eb-115">*Определенные в файле winerror.h файл заголовка пакета SDK Windows.*</span><span class="sxs-lookup"><span data-stu-id="650eb-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="650eb-116">Идентификаторы интерфейса</span><span class="sxs-lookup"><span data-stu-id="650eb-116">Interface identifiers</span></span>

<span data-ttu-id="650eb-117">Следующие идентификаторы интерфейса предполагается макрос DEFINE_GUID определенные в guiddef.h файл заголовка Windows SDK для связи символическое имя GUID с его значение.</span><span class="sxs-lookup"><span data-stu-id="650eb-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="650eb-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="650eb-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="650eb-119">DEFINE_GUID (IID_IEnumFBBlock 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="650eb-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="650eb-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="650eb-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="650eb-121">DEFINE_GUID (IID_IFreeBusyData 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="650eb-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="650eb-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="650eb-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="650eb-123">DEFINE_GUID (IID_IFreeBusySupport 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="650eb-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

