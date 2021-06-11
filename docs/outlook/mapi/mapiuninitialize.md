---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408525"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="2aab8-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="2aab8-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="2aab8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aab8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aab8-105">Decrements the reference count, cleans up and deletes per-instance global data for the MAPI DLL.</span><span class="sxs-lookup"><span data-stu-id="2aab8-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aab8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2aab8-106">Header file:</span></span>  <br/> |<span data-ttu-id="2aab8-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="2aab8-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="2aab8-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="2aab8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2aab8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2aab8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2aab8-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="2aab8-110">Called by:</span></span>  <br/> |<span data-ttu-id="2aab8-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="2aab8-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="2aab8-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2aab8-112">Parameters</span></span>

<span data-ttu-id="2aab8-113">Нет</span><span class="sxs-lookup"><span data-stu-id="2aab8-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="2aab8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2aab8-114">Return value</span></span>

<span data-ttu-id="2aab8-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="2aab8-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2aab8-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="2aab8-116">Remarks</span></span>

<span data-ttu-id="2aab8-117">Клиентская заявка вызывает **функцию MAPIUninitialize,** чтобы прекратить взаимодействие с MAPI, начатое с вызова функции [MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="2aab8-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="2aab8-118">После **вызова MAPIUninitialize** клиент не может делать другие вызовы MAPI.</span><span class="sxs-lookup"><span data-stu-id="2aab8-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="2aab8-119">**MAPIUninitialize** отнимет количество ссылок, а соответствующая функция **MAPIInitialize** прибавляет количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="2aab8-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="2aab8-120">Таким образом, количество вызовов одной функции должно равняться количеству вызовов другой.</span><span class="sxs-lookup"><span data-stu-id="2aab8-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2aab8-121">Вы не можете вызвать **MAPIInitialize** или **MAPIUninitialize** из функции **Win32 DllMain** или любой другой функции, которая создает или прекращает потоки.</span><span class="sxs-lookup"><span data-stu-id="2aab8-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="2aab8-122">Дополнительные сведения см. в [Thread-Safe".](using-thread-safe-objects.md)</span><span class="sxs-lookup"><span data-stu-id="2aab8-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

