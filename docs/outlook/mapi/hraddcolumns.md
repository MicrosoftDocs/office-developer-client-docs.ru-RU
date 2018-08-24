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
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580735"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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

