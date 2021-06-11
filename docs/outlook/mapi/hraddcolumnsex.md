---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427481"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет или перемещает столбцы в начало существующей таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>Parameters

 _lptbl_
  
> [in] Указатель на затрагиваемую таблицу MAPI. 
    
 _lpproptagColumnsNew_
  
> [in] Указатель на [структуру SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств для свойств, которые будут добавлены или перенесены в начало таблицы. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _lpfnFilterColumns_
  
> [in] Указатель на функцию вызова, предоставленную вызываемой. Если параметр  _lpfnFilterColumns_ задан в NULL, не будет выполнен вызов. 
    
 _ptaga_
  
> [in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержающую массив тегов свойств, уже существующих в таблице до того, как свойства будут добавлены или перенесены в начало. **HrAddColumnsEx** передает этот указатель в качестве параметра функции вызова, на который указывает _lpfnFilterColumns._
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался, а указанные столбцы были перемещены или добавлены.
    
## <a name="remarks"></a>Примечания

Свойства, переданные **hrAddColumnsEx** с помощью параметра _lpproptagColumnsNew,_ становятся первыми свойствами, выставленными при последующих вызовах методу [IMAPITable::QueryRows.](imapitable-queryrows.md) Все свойства, ранее указанные в таблице, не указанные в параметре  _lpproptagColumnsNew,_ подвергаются воздействию после всех добавленных и перенесенных свойств. 
  
Если при запросе **QueryRows** какие-либо свойства таблицы не определены, они возвращаются с PT_NULL и идентификатором PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrAddColumnsEx** позволяет звоняшему предоставить функцию вызова для фильтрации столбцов, которые уже были в таблице, например для преобразования строк из типа свойства PT_UNICODE в PT_STRING8. **HrAddColumnsEx** передает указатель на ранее существующий столбец, заданный в качестве параметра для функции вызова. Функция вызова может изменять данные в массиве тегов свойств, но не может добавлять новые теги. 
  
 **HrAddColumnsEx** сначала вызывает функцию вызова, если она предоставлена, затем добавляет или перемещает указанные столбцы и, наконец, вызывает [IMAPITable::SetColumns](imapitable-setcolumns.md). 
  
Параметры  _ввода lpAllocateBuffer_ и  _lpFreeBuffer_ указывают на функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Точные значения указателей, переданных **в HrAddColumnsEx,** зависят от того, является ли вызываемая клиентская заявка или поставщик услуг. Клиент передает указатели на функции MAPI с указанными именами. Поставщик услуг передает указатели, полученные в вызове инициализации или полученные, позвонив по [методу IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md) 
  
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

