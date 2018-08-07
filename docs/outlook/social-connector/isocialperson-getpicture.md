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
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Получает массив байтов, который содержит изображение ресурсов для пользователя. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Параметры

_Рисунок_
  
> [out] Указатель на структуру, которая указывает массив байтов, представляющих ресурсов изображения для пользователя.
    
## <a name="remarks"></a>Замечания

Поддерживается рисунка, ресурсы, в .bmp, JPEG и формат PNG.
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

