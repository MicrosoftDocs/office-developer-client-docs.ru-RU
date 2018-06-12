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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808650"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Применимо к**: Outlook 
  
Добавляет или перемещение столбцов в начало существующей таблицы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов завершился успешно и были перемещены или добавить указанных столбцов.
    
## <a name="remarks"></a>Замечания

Свойства, переданной в **HrAddColumnsEx** с помощью параметра _lpproptagColumnsNew_ становятся первого свойства, предоставляемые на последующий вызов метода [IMAPITable::QueryRows](imapitable-queryrows.md) . Любые свойства ранее в таблице, которые не были указаны в параметре _lpproptagColumnsNew_ , предоставляемые после все свойства добавлены и перемещенные. 
  
Если при вызове **QueryRows** любого свойства таблицы не определены, они будут возвращены с типом свойства PT_NULL и идентификатор свойства PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Функция **HrAddColumnsEx** позволяет вызывающему бесплатной функции обратного вызова для фильтрации столбцов, которые уже были в таблице, например для преобразования строк из тип свойства PT_UNICODE PT_STRING8. **HrAddColumnsEx** передает указатель ранее существующего столбца задайте в качестве параметра функции обратного вызова. Если функция обратного вызова можно изменить данные в массиве тега свойства, но нельзя добавлять новые теги. 
  
 Если один поставляется, а затем добавляет или перемещает указанных столбцов и наконец вызывает [IMAPITable::SetColumns](imapitable-setcolumns.md) **HrAddColumnsEx** сначала вызывается функция обратного вызова. 
  
Входные параметры _lpAllocateBuffer_ и _lpFreeBuffer_ наведите указатель мыши функции [MAPIAllocateBuffer](mapiallocatebuffer.md) и [MAPIFreeBuffer](mapifreebuffer.md) соответственно. Точные значения указатели, переданной в **HrAddColumnsEx** зависят от того, ли вызывающего клиентского приложения или поставщика услуг. Клиент передает указатели функции MAPI с указанными именами. Поставщик службы передает указатели его полученным в его вызовы инициализации и извлечь путем вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

