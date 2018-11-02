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
ms.openlocfilehash: 566a9d23c46ec717eb5eed711fff801b15d49fc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564236"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет или перемещение столбцов в начало существующей таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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

## <a name="parameters"></a>Параметры

 _lptbl_
  
> [in] Указатель на влияет на таблицы MAPI. 
    
 _lpproptagColumnsNew_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив теги свойства для свойств для добавления или перемещения в начало таблицы. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _lpfnFilterColumns_
  
> [in] Указатель на функцию обратного вызова, предоставляемого вызывающим абонентом. Если параметр _lpfnFilterColumns_ имеет значение NULL, обратный вызов не выполняется. 
    
 _ptaga_
  
> [in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий массив тегов свойств, уже существующих в таблице перед свойства при добавлении или перемещено в начале. **HrAddColumnsEx** передается указатель в качестве параметра функции обратного вызова, на который ссылается _lpfnFilterColumns_.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов завершился успешно и были перемещены или добавить указанных столбцов.
    
## <a name="remarks"></a>Примечания

Свойства, переданной в **HrAddColumnsEx** с помощью параметра _lpproptagColumnsNew_ становятся первого свойства, предоставляемые на последующий вызов метода [IMAPITable::QueryRows](imapitable-queryrows.md) . Любые свойства ранее в таблице, которые не были указаны в параметре _lpproptagColumnsNew_ , предоставляемые после все свойства добавлены и перемещенные. 
  
Если при вызове **QueryRows** любого свойства таблицы не определены, они будут возвращены с типом свойства PT_NULL и идентификатор свойства PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrAddColumnsEx** позволяет вызывающему бесплатной функции обратного вызова для фильтрации столбцов, которые уже были в таблице, например для преобразования строк из тип свойства PT_UNICODE PT_STRING8. **HrAddColumnsEx** передает указатель ранее существующего столбца задайте в качестве параметра функции обратного вызова. Если функция обратного вызова можно изменить данные в массиве тега свойства, но нельзя добавлять новые теги. 
  
 Если один поставляется, а затем добавляет или перемещает указанных столбцов и наконец вызывает [IMAPITable::SetColumns](imapitable-setcolumns.md) **HrAddColumnsEx** сначала вызывается функция обратного вызова. 
  
Входные параметры _lpAllocateBuffer_ и _lpFreeBuffer_ наведите указатель мыши функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Точные значения указатели, переданной в **HrAddColumnsEx** зависят от того, ли вызывающего клиентского приложения или поставщика услуг. Клиент передает указатели функции MAPI с указанными именами. Поставщик службы передает указатели его полученным в его вызовы инициализации и извлечь путем вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

