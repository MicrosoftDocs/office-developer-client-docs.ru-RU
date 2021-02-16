---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278836"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет, есть ли у вызываемого процесса доступ на чтение к указанному диапазону памяти.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |mapiwin.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку ASCII, одернутую нулью.
    
 _cchMax_
  
> [in] Максимальный размер строки в chars. Функция проверяет доступ на чтение во всех символах до символа null строки или до числа символов, указанных этим параметром, в зависимости от того, какой символ меньше. Если этот параметр имеет нулевое значение, возвращается нулевое значение.
    
## <a name="return-value"></a>Возвращаемое значение

Возвращаемая величина — нуль, если вызывающий процесс имеет доступ на чтение ко всем символам до символа null строки или доступу на чтение до количества символов, указанных _cchMax._
  
Возвращаемая величина не является нулем, если вызывающий процесс не имеет доступа на чтение ко всем символам до символа нулевых терминов строки или доступу на чтение до количества символов, указанных _cchMax._
  
## <a name="remarks"></a>Примечания

Функция **IsBadBoundedStringPtr** эквивалентна использованию **IsBadStringPtr.**
  
## <a name="see-also"></a>См. также



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

