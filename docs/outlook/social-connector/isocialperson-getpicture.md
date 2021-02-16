---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Получает массив в ветвях, содержащий ресурс рисунка для человека.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406712"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Получает массив в ветвях, содержащий ресурс рисунка для человека. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Параметры

_picture_
  
> [out] Указатель на структуру, указываваю массив ветвей, представляю>ресурс рисунка для человека.
    
## <a name="remarks"></a>Примечания

Поддерживаемые ресурсы изображений в формате BMP, JPEG или PNG.
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

