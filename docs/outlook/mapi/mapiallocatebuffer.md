---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357311"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выделяет буфер памяти. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапикс. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Параметры

 _Кбсизе_
  
> возврата Размер выделяемого буфера (в байтах). 
    
 _Лппбуффер_
  
> вышли Указатель на возвращенный выделенный буфер.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернулся запрошенный буфер памяти.
    
## <a name="remarks"></a>Примечания

Во время обработки вызовов **мапиаллокатебуффер** вызывающая реализация получает блок памяти из операционной системы. Буфер памяти выделяется на байтовый адрес с четным номером. На платформах, где доступ к долговременному целому числу эффективнее, операционная система выделяет буфер на адресе, размер которого в байтах равен четырем. 
  
Вызов функции [мапифрибуффер](mapifreebuffer.md) освобождает буфер памяти, выделенный в **мапиаллокатебуффер**, вызывая функцию [мапиаллокатеморе](mapiallocatemore.md) и все связанные с ней буферы, когда память больше не нужна. 
  
## <a name="see-also"></a>См. также



[MAPIReallocateBuffer](mapireallocatebuffer.md)

