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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Знание того, как и когда распределять и выделять свободную память, является важной частью программирования с помощью MAPI. MAPI предоставляет функции и макрос, которые клиент или поставщик услуг может использовать для последовательного управления памятью. Эти три функции следуют следующим образом:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Когда клиенты и поставщики услуг используют эти функции, устраняется вопрос о том, кто "владеет", то есть знает, как освободиться, — определенный блок памяти. Клиенту, вызываемому методу поставщика услуг, не нужно проходить достаточно большой буфер для удержания значения возврата любого размера. Поставщик служб может просто выделить соответствующее количество памяти с помощью **MAPIAllocateBuffer** и, при необходимости, **MAPIAllocateMore,** и клиент может позже выпустить ее по завеству с помощью **MAPIFreeBuffer,** независимо от поставщика услуг. 
  
Макрос памяти используется для выделения структур или массивов структур определенного размера. Клиенты и поставщики услуг должны использовать эти макрос, а не распределять память вручную. Например, если клиенту необходимо выполнить обработку разрешения имен в списке получателей с тремя записями, макрос **SizedADRLIST** можно использовать для создания структуры **ADRLIST,** чтобы передать **В IAddrBook::ResolveName** с правильным числом **участников ADRENTRY.** Все макрос памяти определяются в MAPIDEFS. Файл заглавной папки H. Эти макрос: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI также поддерживает использование интерфейса [COM IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) для управления памятью. Поставщики услуг получили указатель **интерфейса IMalloc** по MAPI во время инициализации и могут также получить его с помощью [функции MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md) Основное преимущество использования методов **IMalloc** для управления памятью над функциями MAPI заключается в том, что с помощью методов COM можно перенаправить существующий буфер. Функции памяти MAPI не поддерживают перераспределение. 
  

