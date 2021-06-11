---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410555"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освободит буфер памяти, выделенный с помощью вызова функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или [функции MAPIAllocateMore.](mapiallocatemore.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parameters

 _lpBuffer_
  
> [in] Указатель на ранее выделенный буфер памяти. Если NULL передается в  _параметре lpBuffer,_ **MAPIFreeBuffer** ничего не делает. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и освободил запрашиваемую память. **MAPIFreeBuffer** также может возвращать S_OK уже освобожденных расположениях или если блок памяти не выделен **с MAPIAllocateBuffer** и **MAPIAllocateMore**.
    
## <a name="remarks"></a>Примечания

Обычно, когда клиентские приложения или поставщик услуг вызывает [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore,](mapiallocatemore.md)операционная система строит в одном соразмерном буфере памяти одну или несколько сложных структур с несколькими уровнями указателей. Когда функция MAPI или метод создает буфер с таким содержимым, клиент может освободить все структуры, содержащиеся в буфере, передав **MAPIFreeBuffer** указатель в буфер, возвращенный функцией MAPI, создав буфер. Чтобы поставщик службы освободил буфер памяти с помощью **MAPIFreeBuffer,** он должен передать указатель в буфер, возвращенный с помощью объекта поддержки поставщика. 
  
Вызов **MAPIFreeBuffer,** чтобы освободить определенный буфер, должен быть выполнен сразу после завершения использования этого буфера клиентом или поставщиком. Просто вызов [метода IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI автоматически не освобождает буферы памяти. 
  
Клиент или поставщик услуг должны работать с предположением о том, что указатель, переданный _в lpBuffer,_ недействителен после успешного возвращения **из MAPIFreeBuffer.** Если указатель указывает либо блок памяти, не выделенный системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore,** либо свободный блок памяти, поведение **MAPIFreeBuffer** неопределяется. 
  
> [!NOTE]
> Передача указателя null в **MAPIFreeBuffer** упрощает и меньше код очистки приложений, так как **MAPIFreeBuffer** может инициализировать указатели в NULL, а затем освободить их в коде очистки, не тестировать их сначала. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

