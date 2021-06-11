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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Требование о выделении всей памяти для буфера по возможности одним вызовом **MAPIAllocateBuffer** не применяется при использовании списка адресов или **ADRLIST** и набора строк или **структур SRowSet.** 
  
Эти две структуры являются исключениями из стандартных правил выделения и выпуска памяти. Они содержат несколько уровней структур и предназначены для того, чтобы позволить отдельным участникам добавляться или удаляться. Поэтому каждое свойство должно быть отдельным распределением. 

Если большинство структур освобождены одним вызовом **в MAPIFreeBuffer,** каждая индивидуальная запись в **структуре ADRLIST** или **SRowSet** должна быть освобождена со своим собственным вызовом **MAPIFreeBuffer** или одним вызовом для **freeProws** или **FreePadrlist**. Дополнительные сведения см. [в mapIFreeBuffer,](mapifreebuffer.md) [ADRLIST](adrlist.md)и [SRowSet.](srowset.md) 

**FreeProws и** **FreePadrlist** — это функции, предоставляемые MAPI для упрощения работы с этими структурами данных. Дополнительные сведения см. [в списках FreeProws и](freeprows.md) [FreePadrlist.](freepadrlist.md) **FreePadrlist** освободит память для **структуры ADRLIST** плюс все связанные памяти для членов структуры; **FreeProws делает** то же самое для **структуры SRowSet.** 
  
На следующей схеме показан макет структуры **данных ADRLIST,** указывающая на необходимые отдельные выделения памяти. Серые поля показывают память, которую можно выделить и освободить одним вызовом. 
  
**Выделение памяти ADRLIST**
  
![Распределение памяти ADRLIST](media/amapi_52.gif "ADRLIST")
  
## <a name="see-also"></a>См. также

- [Управление памятью в MAPI](managing-memory-in-mapi.md)

