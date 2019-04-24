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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328016"
---
# <a name="freeprows"></a>FreeProws

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Уничтожает структуру [SRowSet](srowset.md) и освобождает связанную память, в том числе память, выделенную для всех массивов и структур элементов. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Параметры

 _провс_
  
> возврата Указатель на структуру **SRowSet** , которую необходимо уничтожить. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В рамках реализации **фрипровс**MAPI вызывает функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить каждую запись в структуре **SRowSet** , прежде чем освобождать всю структуру. Таким образом, все такие записи должны следовать правилам распределения для структуры [SRowSet](srowset.md) , используя отдельный вызов [мапиаллокатебуффер](mapiallocatebuffer.md) для каждого массива и структуры элементов. 
  
Дополнительные сведения о выделении памяти для структур **ADRLIST** и **SRowSet** можно найти в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстаблелистктрл. cpp  <br/> |Двсреадфунклоадтабле  <br/> |MFCMAPI использует метод **фрипровс** для освобождения структуры SRowSet, содержащей строки обрабатываемой таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

