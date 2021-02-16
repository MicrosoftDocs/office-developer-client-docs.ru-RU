---
title: Управление памятью для структур ADRLIST и SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407867"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Управление памятью для структур ADRLIST и SRowSet"

**Относится к**: Outlook 2013 | Outlook 2016 
  
Требование выделить всю память для буфера по возможности с помощью одного вызова **MAPIAllocateBuffer** не применяется при использовании списка адресов, **ADRLIST** и набора строк, или **SRowSet**, структур. 
  
Эти две структуры являются исключениями из стандартных правил для выделения и освобождения памяти. Они содержат несколько уровней структур и предназначены для того, чтобы добавлять или удалять отдельные члены. Поэтому каждое свойство должно быть выделено отдельно. 

Если большинство структур освобождены с помощью одного вызова **MAPIFreeBuffer,** каждая запись в **структуре ADRLIST** или **SRowSet** должна быть освобождена с помощью собственного вызова **MAPIFreeBuffer** или одного вызова **FreeProws** или **FreePadrlist**. Дополнительные сведения см. в [mapIFreeBuffer,](mapifreebuffer.md) [ADRLIST](adrlist.md)и [SRowSet.](srowset.md) 

**FreeProws** и **FreePadrlist** — это функции, предоставляемые MAPI для упрощения освободить эти структуры данных. Дополнительные сведения [см. в записях FreeProws](freeprows.md) и [FreePadrlist.](freepadrlist.md) **FreePadrlist** освободит память для структуры **ADRLIST** и всю связанную память для членов структуры; **FreeProws** делает то же самое для **структуры SRowSet.** 
  
На следующей схеме показана структура **данных ADRLIST,** указывающая на отдельные необходимые объемы памяти. Серые поля показывают память, которую можно выделить и освободить одним вызовом. 
  
**Выделение памяти ADRLIST**
  
![Выделение памяти ADRLIST для](media/amapi_52.gif "выделения памяти ADRLIST")
  
## <a name="see-also"></a>См. также

- [Управление памятью в MAPI](managing-memory-in-mapi.md)

