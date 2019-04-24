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
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Возвращает массив байтов, который содержит ресурс изображения для пользователя. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Параметры

_графические_
  
> вышли Указатель на структуру, задающую массив байтов, представляющий ресурс изображения для человека.
    
## <a name="remarks"></a>Комментарии

Поддерживаются графические ресурсы в формате BMP, JPEG или PNG.
  
## <a name="see-also"></a>См. также

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

