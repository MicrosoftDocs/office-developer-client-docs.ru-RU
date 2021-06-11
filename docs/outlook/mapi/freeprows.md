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
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438822"
---
# <a name="freeprows"></a>FreeProws

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уничтожает [структуру SRowSet](srowset.md) и освободит связанную память, включая память, выделенную для всех массивов и структур членов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parameters

 _prows_
  
> [in] Указатель на **структуру SRowSet,** которая будет уничтожена. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В рамках своей реализации **FreeProws** MAPI вызывает функцию [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить каждую запись в **структуре SRowSet,** прежде чем освободить полную структуру. Поэтому все такие записи должны следовать правилам распределения для структуры [SRowSet,](srowset.md) используя отдельный вызов [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого массива и структуры участников. 
  
Дополнительные сведения о деление памяти для структур **ADRLIST** и **SRowSet** см. в рубрике Управление памятью для [структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI использует **метод FreeProws,** чтобы освободить структуру SRowSet, содержащую строки обрабатываемой таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

