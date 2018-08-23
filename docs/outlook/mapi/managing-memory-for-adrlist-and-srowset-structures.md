---
title: Управление памятью для структуры ADRLIST и SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589730"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Управление памятью для структуры ADRLIST и SRowSet»

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Требования для выделения памяти все буфера, когда это возможно с помощью одного вызова **MAPIAllocateBuffer** не применяется при использовании списка адресов или **ADRLIST**и набор строк или **SRowSet**структуры. 
  
Эти две структуры, исключения из стандартного правил для распределения и освобождения памяти. Они содержат несколько уровней структуры, которые предназначены для включения отдельные элементы, чтобы добавить или удалить. Таким образом каждое свойство должно быть отдельные выделения. 

Где большинство структур высвобождаются с помощью одного вызова к **MAPIFreeBuffer**, каждая отдельная запись **ADRLIST** или **SRowSet** структура освобождения с собственной вызов **MAPIFreeBuffer** или один вызов **FreeProws** или ** FreePadrlist**. Для получения дополнительных сведений см [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)и [SRowSet](srowset.md). 

**FreeProws** и **FreePadrlist** являются функций, предоставляемых MAPI для упрощения освобождение эти структуры данных. Для получения дополнительных сведений см [FreeProws](freeprows.md) и [FreePadrlist](freepadrlist.md). **FreePadrlist** освобождает память для структуры **ADRLIST** , а также все связанные с ним памяти членов структуры. **FreeProws** делает то же самое для структуры **SRowSet** . 
  
На следующей схеме показана макет структуру данных **ADRLIST** , указывающее, отдельные необходимые там. Серая поля показывают объем памяти, который можно выделить и выпущен с помощью одного вызова. 
  
**Выделение памяти ADRLIST**
  
![Выделение памяти adrlist] (media/amapi_52.gif "Выделение памяти adrlist")
  
## <a name="see-also"></a>См. также

- [Управление памятью в MAPI](managing-memory-in-mapi.md)

