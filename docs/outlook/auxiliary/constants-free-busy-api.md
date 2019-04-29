---
title: Константы (API сведений о доступности)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейсов для API сведений о доступности.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431535"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="b9481-103">Константы (API сведений о доступности)</span><span class="sxs-lookup"><span data-stu-id="b9481-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="b9481-104">В этом разделе содержатся определения констант, идентификаторы классов и идентификаторы интерфейсов для API сведений о доступности.</span><span class="sxs-lookup"><span data-stu-id="b9481-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="b9481-105">Константы</span><span class="sxs-lookup"><span data-stu-id="b9481-105">Constants</span></span>

|<span data-ttu-id="b9481-106">**Константа**</span><span class="sxs-lookup"><span data-stu-id="b9481-106">**Constant**</span></span>|<span data-ttu-id="b9481-107">**Определение**</span><span class="sxs-lookup"><span data-stu-id="b9481-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9481-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="b9481-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="b9481-109">*Как определено в файле заголовков пакета средств разработки программного обеспечения (SDK) для Microsoft Windows (SDK) Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="b9481-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="b9481-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b9481-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="b9481-111">*Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="b9481-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="b9481-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b9481-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="b9481-113">*Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="b9481-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="b9481-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9481-114">S_OK</span></span>  <br/> | <span data-ttu-id="b9481-115">*Как указано в файле заголовка пакета SDK для Windows, как указано в файле Winerror. h.*</span><span class="sxs-lookup"><span data-stu-id="b9481-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="b9481-116">Идентификаторы интерфейсов</span><span class="sxs-lookup"><span data-stu-id="b9481-116">Interface identifiers</span></span>

<span data-ttu-id="b9481-117">Для следующих идентификаторов интерфейса предположим, что макрос ДЕФИНЕ_ГУИД, определенный в файле заголовка Windows SDK guiddef. h, связывает символьное имя GUID со значением.</span><span class="sxs-lookup"><span data-stu-id="b9481-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="b9481-118">{00067064-0000-0000 — C000 — 000000000046}</span><span class="sxs-lookup"><span data-stu-id="b9481-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="b9481-119">ДЕФИНЕ_ГУИД (Иид_иенумфбблокк, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="b9481-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="b9481-120">{00067066-0000-0000 — C000 — 000000000046}</span><span class="sxs-lookup"><span data-stu-id="b9481-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="b9481-121">ДЕФИНЕ_ГУИД (Иид_ифрибусидата, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="b9481-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="b9481-122">{00067067-0000-0000 — C000 — 000000000046}</span><span class="sxs-lookup"><span data-stu-id="b9481-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="b9481-123">ДЕФИНЕ_ГУИД (Иид_ифрибусисуппорт, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span><span class="sxs-lookup"><span data-stu-id="b9481-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

