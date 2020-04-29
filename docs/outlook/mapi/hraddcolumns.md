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
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422476"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет или перемещает столбцы в начало существующей таблицы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Параметры

 _лптбл_
  
> возврата Указатель на таблицу MAPI, на которую вы затронули.
    
 _лппроптагколумнснев_
  
> возврата Указатель на структуру **спроптагаррай** , которая содержит массив тегов свойств для добавления или перемещения свойств в начало таблицы. 
    
 _лпаллокатебуффер_
  
> возврата Указатель на функцию **мапиаллокатебуффер** . Используется для выделения памяти. 
    
 _лпфрибуффер_
  
> возврата Указатель на функцию **мапифрибуффер** . Используется для освобождения памяти. 
    
## <a name="return-value"></a>Возвращаемое значение

 **S_OK**
  
> Вызов выполнен успешно, и указанные столбцы были перемещены или добавлены.
    
## <a name="remarks"></a>Примечания

Функция **храддколумнс** эквивалентна использованию **храддколумнсекс** с параметром _лпфнфилтерколумнс_ , равным null. 
  
## <a name="see-also"></a>См. также



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

