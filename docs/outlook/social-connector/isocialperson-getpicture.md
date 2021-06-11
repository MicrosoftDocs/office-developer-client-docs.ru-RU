---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Получает массив bytes, который содержит ресурс изображения для человека.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406712"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="714d4-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="714d4-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="714d4-104">Получает массив bytes, который содержит ресурс изображения для человека.</span><span class="sxs-lookup"><span data-stu-id="714d4-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="714d4-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="714d4-105">Parameters</span></span>

<span data-ttu-id="714d4-106">_изображение_</span><span class="sxs-lookup"><span data-stu-id="714d4-106">_picture_</span></span>
  
> <span data-ttu-id="714d4-107">[вышел] Указатель на структуру, которая указывает массив bytes, которые представляют ресурс изображения для человека.</span><span class="sxs-lookup"><span data-stu-id="714d4-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="714d4-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="714d4-108">Remarks</span></span>

<span data-ttu-id="714d4-109">Поддерживаемые ресурсы изображений находятся в .bmp, jpeg или .png формате.</span><span class="sxs-lookup"><span data-stu-id="714d4-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="714d4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="714d4-110">See also</span></span>

- [<span data-ttu-id="714d4-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="714d4-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

