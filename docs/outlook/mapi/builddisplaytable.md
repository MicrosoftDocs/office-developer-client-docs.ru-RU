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
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577690"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает таблицу, отображаемое на основе данных страницы свойств, содержащихся в одной или нескольких структур [DTPAGE](dtpage.md) . 
  
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
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _lpMalloc_
  
> Неиспользуемые; должен иметь значение NULL. 
    
 _hInstance_
  
> [in] Экземпляр объекта MAPI, из которого **BuildDisplayTable** извлекает ресурсы. 
    
 _cPages_
  
> [in] Число структур [DTPAGE](dtpage.md) в массиве указывает параметр _lpPage_ . 
    
 _lpPage_
  
> [in] Указатель на массив структур **DTPAGE** , которые содержат сведения о страницах в таблице отображения для построения. 
    
 _ulFlags_
  
> [in] Битовая маска флаги. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppTable_
  
> [out] Указатель на указатель в таблице отображения, который предоставляет интерфейс [IMAPITable](imapitableiunknown.md) . 
    
 _lppTblData_
  
> [in, out] Указатель на указатель на объект данных в таблице, предоставление интерфейс [ITableData](itabledataiunknown.md) в таблице, возвращаемой в параметре _lppTable_ . В случае необходимости объект данных не в таблице _lppTblData_ должно быть присвоено значение NULL вместо значение указателя. 
    
## <a name="return-value"></a>Возвращаемое значение

Отсутствует
  
## <a name="remarks"></a>Замечания

Функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти, в частности для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объектной использует MAPI Например, [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Все возможности считываются из диалогового окна ресурсов, включая:
  
- Заголовок страницы, который является, член _ulbLpszLabel_ структуры [DTBLPAGE](dtblpage.md) чтение из заголовка диалогового окна в ресурсе. 
    
- Все заголовки элемента управления, которым будет, _ulbLpszLabel_ члены других структур элементов управления, чтение из текста элемента управления в ресурсе. 
    
 **BuildDisplayTable** перезаписывает что-либо переданную структур управления ввода со сведениями из ресурс диалогового окна, что означает, что Звонящий **BuildDisplayTable** нельзя задать динамически заголовков страницы или элемента управления. Абоненты, которые необходимо сделать, у которых есть **BuildDisplayTable** возвращает объект данных в таблице в _lppTableData_ и измените строк в нем; или они вместо построения в таблице отображения вручную в объекте таблицы данных. 
  
Если _lppTableData_ не задано значение NULL, поставщик несет ответственность за освобождение объект данных в таблице при завершении работы с таблицей отображения. 
  

