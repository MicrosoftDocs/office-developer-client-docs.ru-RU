---
title: ИсоЦиалперсонжетпиктуре
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Возвращает массив байтов, который содержит ресурс изображения для пользователя.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331656"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="a6611-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="a6611-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="a6611-104">Возвращает массив байтов, который содержит ресурс изображения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a6611-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="a6611-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6611-105">Parameters</span></span>

<span data-ttu-id="a6611-106">_графические_</span><span class="sxs-lookup"><span data-stu-id="a6611-106">_picture_</span></span>
  
> <span data-ttu-id="a6611-107">вышли Указатель на структуру, задающую массив байтов, представляющий ресурс изображения для человека.</span><span class="sxs-lookup"><span data-stu-id="a6611-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6611-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6611-108">Remarks</span></span>

<span data-ttu-id="a6611-109">Поддерживаются графические ресурсы в формате BMP, JPEG или PNG.</span><span class="sxs-lookup"><span data-stu-id="a6611-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6611-110">См. также</span><span class="sxs-lookup"><span data-stu-id="a6611-110">See also</span></span>

- [<span data-ttu-id="a6611-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6611-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

