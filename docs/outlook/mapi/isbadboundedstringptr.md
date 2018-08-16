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
ms.openlocfilehash: 0e4e5d5910a7ff3551057760f065e79155d65e49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809579"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Относится к**: Outlook 
  
Проверяет, что вызывающий процесс имеет доступ на чтение для указанного диапазона памяти.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |mapiwin.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку ASCII символом null.
    
 _cchMax_
  
> [in] Максимальный размер строки в символах. Функция проверяет наличие доступ на чтение в все символы до выполнения определенного пустого строки или до числа символов, указанных в этом параметре, какое из значений меньше. Если этот параметр равно нулю, возвращаемое значение равно нулю.
    
## <a name="return-value"></a>������������ ��������

Возвращаемое значение равно нулю, когда процесс вызова имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.
  
Значение, возвращаемое при ненулевое процесс вызова не имеет доступ на чтение к все символы до выполнения определенного пустого строки или доступ на чтение до числа знаков, указанное в _cchMax_.
  
## <a name="remarks"></a>Замечания

Функция **IsBadBoundedStringPtr** эквивалентно использованию **IsBadStringPtr**.
  
## <a name="see-also"></a>См. также



[IsBadStringPtr](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)
