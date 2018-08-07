---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808644"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Относится к**: Outlook 
  
Добавляет или перемещение столбцов в начало существующей таблицы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Параметры

 _lptbl_
  
> [in] Указатель на влияет на таблицы MAPI.
    
 _lpproptagColumnsNew_
  
> [in] Указатель на структуру **SPropTagArray** , который содержит массив теги свойства для свойств для добавления или перемещения в начало таблицы. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию **MAPIAllocateBuffer** . Используется для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию **MAPIFreeBuffer** . Используется, чтобы освободить память. 
    
## <a name="return-value"></a>������������ ��������

 **ЗНАЧЕНИЕ S_OK**
  
> Вызов завершился успешно и были перемещены или добавить указанных столбцов.
    
## <a name="remarks"></a>Замечания

Функция **HrAddColumns** эквивалентно использованию **HrAddColumnsEx** с _lpfnFilterColumns_ задано значение NULL. 
  
## <a name="see-also"></a>См. также



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

