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
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809898"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Относится к**: Outlook 
  
Освобождает буфер памяти, выделенный с помощью вызова функции [MAPIAllocateBuffer](mapiallocatebuffer.md) или функцию [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Параметры

 _lpBuffer_
  
> [in] Указатель на буфер ранее выделенной памяти. Если значение NULL передается в параметре _lpBuffer_ , **MAPIFreeBuffer** не имеет никакого эффекта. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и освобождается память запрошено. **MAPIFreeBuffer** может также возвращать значение S_OK на уже освобожденное расположения или если блок памяти не выделяется с **MAPIAllocateBuffer** и **MAPIAllocateMore**.
    
## <a name="remarks"></a>Замечания

Как правило, когда клиентского приложения или поставщика услуг вызывает метод [MAPIAllocateBuffer](mapiallocatebuffer.md) или [MAPIAllocateMore](mapiallocatemore.md), конструкции операционной системы в одной непрерывной памяти буфера один или несколько сложных структур с несколькими уровнями указатели. Когда функция MAPI или метод создает буфер с таким содержимым, клиента более поздней версии можно освободить все структуры, содержащихся в буфере, передав **MAPIFreeBuffer** указатель на буфер, возвращаемого функцией MAPI, которые созданы буфер. Для поставщика услуг освободить память буфера, используя **MAPIFreeBuffer**его необходимо передать указатель буфером, возвращаемых в объект поддержки поставщика. 
  
Вызов **MAPIFreeBuffer** для освобождения определенного буфера должна состоять как можно скорее клиента или поставщика по завершении работы с помощью этого буфера. Просто вызов метода [IMAPISession::Logoff](imapisession-logoff.md) в конце сеанса MAPI не освобождает автоматически буферов памяти. 
  
Предварительное условие, указатель, переданный _lpBuffer_ является недопустимым после успешного возвращения из **MAPIFreeBuffer**следует работать клиента или поставщика. Если указатель мыши указывает блок памяти, не выделяются системой обмена сообщениями через **MAPIAllocateBuffer** или **MAPIAllocateMore** или блок свободной памяти, поведение **MAPIFreeBuffer** не определено. 
  
> [!NOTE]
> Передача указатель на значение null, в **MAPIFreeBuffer** делает код очистки приложения проще и меньшего размера так, как можно инициализировать указатели на значение NULL и освободить их код очистки без необходимости их необходимо протестировать сначала **MAPIFreeBuffer** . 
  
## <a name="see-also"></a>См. также



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

