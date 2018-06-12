---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- функция fdance [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807260"
---
# <a name="fdance"></a>fDance

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской команды, изменения выбранных ячеек на активном листе вокруг только при нажатии клавиши **ESC**. При загрузке GENERIC.xll, он создает пользовательских меню, общая, через который доступ к этой команды.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameters

Функция не принимает параметры.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Функция всегда возвращает 1.
  
## <a name="remarks"></a>Замечания

Это пример длительной операции. Периодически вызывает функцию [xlAbort](xlabort.md) . Это дает процессора (помощь с совместной работой многозадачность) и проверяет нажатии пользователем клавиши **ESC** , чтобы отменить операцию. Если это так, предлагает пользователю возможность отменить аварийное завершение. 
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

