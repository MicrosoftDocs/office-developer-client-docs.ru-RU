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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Освободить буфер памяти, выделенный вызовом функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore.](mapiallocatemore.md) 
  
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

## <a name="parameters"></a>Параметры

 _lpBuffer_
  
> [in] Указатель на ранее выделенный буфер памяти. Если в параметре  _lpBuffer_ передается NULL, **MAPIFreeBuffer** ничего не делает. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и освобожден запрашиваемой памяти. **MAPIFreeBuffer** также может возвращать S_OK уже освобожденных расположениях или если блок памяти не выделен с **помощью MAPIAllocateBuffer** и **MAPIAllocateMore.**
    
## <a name="remarks"></a>Примечания

Обычно, когда клиентский приложение или поставщик услуг вызывает [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore,](mapiallocatemore.md)операционная система строит в одном буфере памяти одну или несколько сложных структур с несколькими уровнями указателей. Когда функция или метод MAPI создает буфер с таким содержимым, клиент позднее может освободить все структуры, содержащиеся в буфере, передав **MAPIFreeBuffer** указатель на буфер, возвращенный функцией MAPI, которая создала буфер. Чтобы поставщик услуг освободил буфер памяти с помощью **MAPIFreeBuffer,** он должен передать указатель в этот буфер, возвращенный объектом поддержки поставщика. 
  
Вызов **MAPIFreeBuffer** для освободить определенный буфер должен быть выполнен, как только клиент или поставщик завершит использование этого буфера. Вызов метода [IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI не освобождает автоматически буферы памяти. 
  
Клиент или поставщик услуг должен работать, предполагая, что указатель, переданный _в lpBuffer,_ недействителен после успешного возврата **от MAPIFreeBuffer.** Если указатель указывает на блок памяти, не выделенный системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore,** либо на свободный блок памяти, поведение **MAPIFreeBuffer** будет неопределенным. 
  
> [!NOTE]
> Передача NULL-указателя в **MAPIFreeBuffer** упрощает и меньше кода очистки приложения, так как **MAPIFreeBuffer** может инициализировать указатели на NULL, а затем освободить их в коде очистки, не тестировать их в первую очередь. 
  
## <a name="see-also"></a>См. также



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

