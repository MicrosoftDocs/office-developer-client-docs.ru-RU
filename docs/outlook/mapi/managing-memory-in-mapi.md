---
title: Управление памятью в MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298098"
---
# <a name="managing-memory-in-mapi"></a>Управление памятью в MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Знание того, как и когда выделять и освободить память, является важной частью программирования с помощью MAPI. MAPI предоставляет функции и макрос, которые клиент или поставщик услуг может использовать для согласованного управления памятью. Эти три функции:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Когда клиенты и поставщики услуг используют эти функции, устраняется проблема с тем, кто является владельцем, то есть знает, как освободить определенный блок памяти. Клиенту, вызываемому методу поставщика услуг, не требуется передавать буфер, достаточный для удержания возвращаемого значения любого размера. Поставщик услуг может просто выделить соответствующий объем памяти с помощью **MAPIAllocateBuffer** и, при необходимости, **MAPIAllocateMore,** и клиент позднее может освободить его с помощью **MAPIFreeBuffer** независимо от поставщика услуг. 
  
Макрос памяти используется для выделения структур или массивов структур определенного размера. Клиенты и поставщики услуг должны использовать эти макрос, а не выделять память вручную. Например, если клиенту необходимо выполнить обработку разрешения имен в списке получателей с тремя записями, макрос **SizedADRLIST** можно использовать для создания структуры **ADRLIST,** которая будет передана в **IAddrBook::ResolveName** с правильным числом членов **ADRENTRY.** Все макросы памяти определены в MAPIDEFS. Файл h-загона. Эти макросы: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI также поддерживает использование интерфейса COM [IMalloc для](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) управления памятью. Поставщики услуг имеют указатель **интерфейса IMalloc** с помощью MAPI во время инициализации и могут получить его с помощью функции [MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md) Основное преимущество использования методов **IMalloc** для управления памятью по сравнению с функциями MAPI заключается в том, что с помощью методов COM можно перенаправить существующий буфер. Функции памяти MAPI не поддерживают перераспределение данных. 
  

