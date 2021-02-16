---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431598"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает таблицу отображения из данных страницы свойств, содержащихся в одной или более [структурах DTPAGE.](dtpage.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>Параметры

 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _lpMalloc_
  
> Неиспользовано; должно быть установлено в NULL. 
    
 _hInstance_
  
> [in] Экземпляр объекта MAPI, из которого **BuildDisplayTable** извлекает ресурсы. 
    
 _cPages_
  
> [in] Количество структур [DTPAGE](dtpage.md) в массиве, на который указывает параметр _lpPage._ 
    
 _lpPage_
  
> [in] Указатель на массив структур **DTPAGE,** содержащих сведения о страницах таблиц отображения, которые необходимо построить. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу отображения, которая предоставляет [интерфейс IMAPITable.](imapitableiunknown.md) 
    
 _lppTblData_
  
> [in, out] Указатель на указатель на объект данных таблицы, который является интерфейсом [ITableData](itabledataiunknown.md) в таблице, возвращаемой в _параметре lppTable._ Если объект данных таблицы не требуется, следует установить  _для lppTblData_ значение NULL вместо значения указателя. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет
  
## <a name="remarks"></a>Примечания

MAPI использует функции, на которые указывают  _lpAllocateBuffer_,  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения большей части памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В ресурсе диалогового окна считыно все возможное, в том числе:
  
- Заголовок страницы, т. е. член  _ulbLpszLabel_ структуры [DTBLPAGE,](dtblpage.md) считываемой из заголовка диалоговых окно в ресурсе. 
    
- Все заголовки, то есть  _члены ulbLpszLabel_ других структур управления, считываемого из текста управления в ресурсе. 
    
 **BuildDisplayTable** перезаписает все данные, переданные в структурах управления входными данными, с данными из ресурса диалоговых окной, что означает, что вызывающая стороны **BuildDisplayTable** не может динамически указывать заголовки страниц или управления. Звонявшие, которым необходимо это сделать, могут **получить объект данных таблицы в**  _lppTableData_ и изменить строки в нем; или они могут создать отображаемую таблицу вручную в объекте данных таблицы. 
  
Если  _для lppTableData_ не задано NULL, поставщик отвечает за то, чтобы освободить объект данных таблицы после его завершения с таблицей отображения. 
  

