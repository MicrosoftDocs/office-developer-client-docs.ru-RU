---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578026"
---
# <a name="freeprows"></a>FreeProws

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Удаляет структуру [SRowSet](srowset.md) и освобождает связанные памяти, включая объем памяти, выделенный для всех элементов массивов и структур. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Параметры

 _prows_
  
> [in] Указатель на структуру **SRowSet** удалена. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Как часть его реализация **FreeProws**MAPI вызывает функцию [MAPIFreeBuffer](mapifreebuffer.md) для освобождения каждой записи в структуре **SRowSet** перед очисткой полной структурой. Таким образом все записи следует правила распределения для структуры [SRowSet](srowset.md) , с помощью отдельного вызова [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого элемента массива и структуры. 
  
Дополнительные сведения о выделении памяти для структуры **ADRLIST** и **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |Mfcmapi (en) использует метод **FreeProws** , чтобы освободить место на структуру SRowSet, содержащую строки в таблице, обрабатываемых.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

