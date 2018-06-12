---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Получает массив байтов, который содержит изображение ресурсов для пользователя.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812718"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="014a8-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="014a8-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="014a8-104">Получает массив байтов, который содержит изображение ресурсов для пользователя.</span><span class="sxs-lookup"><span data-stu-id="014a8-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="014a8-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="014a8-105">Parameters</span></span>

<span data-ttu-id="014a8-106">_Рисунок_</span><span class="sxs-lookup"><span data-stu-id="014a8-106">_picture_</span></span>
  
> <span data-ttu-id="014a8-107">[out] Указатель на структуру, которая указывает массив байтов, представляющих ресурсов изображения для пользователя.</span><span class="sxs-lookup"><span data-stu-id="014a8-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="014a8-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="014a8-108">Remarks</span></span>

<span data-ttu-id="014a8-109">Поддерживается рисунка, ресурсы, в .bmp, JPEG и формат PNG.</span><span class="sxs-lookup"><span data-stu-id="014a8-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="014a8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="014a8-110">See also</span></span>

- [<span data-ttu-id="014a8-111">ISocialPerson: IUnknown</span><span class="sxs-lookup"><span data-stu-id="014a8-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

