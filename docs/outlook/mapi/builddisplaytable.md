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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _lpMalloc_
  
> Неиспользована; должно быть установлено nULL. 
    
 _hInstance_
  
> [in] Экземпляр объекта MAPI, из которого **BuildDisplayTable** извлекает ресурсы. 
    
 _cPages_
  
> [in] Количество структур [DTPAGE](dtpage.md) в массиве, на который указывает _параметр lpPage._ 
    
 _lpPage_
  
> [in] Указатель на массив структур **DTPAGE,** содержащих сведения о строимой таблице отображения. 
    
 _ulFlags_
  
> [in] Bitmask флагов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Переданные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу отображения, которая предоставляет [интерфейс IMAPITable.](imapitableiunknown.md) 
    
 _lppTblData_
  
> [in, out] Указатель на указатель на объект данных таблицы, подвергая [интерфейсу ITableData](itabledataiunknown.md) на таблице, возвращаемой в _параметре lppTable._ Если объект данных таблицы не требуется, вместо значения указателя следует установить _значение NULL._ 
    
## <a name="return-value"></a>Возвращаемое значение

Нет
  
## <a name="remarks"></a>Примечания

MAPI использует функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для большинства распределений памяти и распределения, в частности для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Все возможное читается из диалогового ресурса, в том числе:
  
- Название страницы, которое является членом  _ulbLpszLabel_ структуры [DTBLPAGE,](dtblpage.md) прочитано из заголовка диалогов на ресурсе. 
    
- Все заголовки управления, которые являются  _ulbLpszLabel_ членами других структур управления, читают из текста управления на ресурсе. 
    
 **BuildDisplayTable** перезаписывал все, что передается в структурах управления входом, с информацией из диалоговых ресурсов, что означает, что вызываемый **в BuildDisplayTable** не может динамически указать заголовки страниц или управления. Звонившие, которым необходимо это сделать, могут иметь **объект BuildDisplayTable** для возврата объекта данных таблицы  _в lppTableData_ и изменения строк в нем; или они могут создавать таблицу отображения вручную в объекте данных таблицы. 
  
Если  _lppTableData_ не установлен в NULL, поставщик несет ответственность за то, чтобы освободить объект данных таблицы по завершению со таблицей отображения. 
  

