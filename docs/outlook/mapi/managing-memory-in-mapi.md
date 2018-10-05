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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388072"
---
# <a name="managing-memory-in-mapi"></a>Управление памятью в MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Знать, как и когда для размещения и освободить память является важной частью программирования с использованием MAPI. MAPI предоставляет функции и макросы, которые ваш поставщик клиента или службы можно использовать для управления памяти в едином виде. Три функции, как показано ниже:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Когда использовать эти функции проблемы клиентов и поставщиков услуг из «владельца» — то есть, знает, как освободить — устранены определенный блок памяти. Клиента, вызывающего метод поставщика службы не нужно передавать буфера, достаточное для хранения возвращаемого значения любого размера. Поставщик услуг просто можно выделить соответствующий объем памяти, с помощью **MAPIAllocateBuffer** и, при необходимости, **MAPIAllocateMore**и клиента можно более поздней версии выпуска его на использование **MAPIFreeBuffer**, вне зависимости от службы будут Поставщик. 
  
Макросы памяти используются для распределения структур или массивов структур определенного размера. Клиенты и поставщиков услуг должен использовать эти макросы, а не вручную выделить память. Например если клиент должен выполнять разрешение имен обработки в список получателей с тремя записями, макрос **SizedADRLIST** можно использовать для создание структуры **ADRLIST** для передачи **IAddrBook::ResolveName** с правильным числом Члены **ADRENTRY** . Все макросы памяти определены в MAPIDEFS. Файл заголовка. Эти макросы являются: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
Использование интерфейса COM [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) также поддерживает MAPI для управления памятью. Поставщики услуг назначается указатель интерфейса **IMalloc** с MAPI во время инициализации, а также можно получить от 1 до [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) функции. Основное преимущество с помощью методов **IMalloc** для управления памяти функции MAPI — это, что с методами COM можно перемещать существующий буфер. Функции памяти MAPI не поддерживают перераспределения. 
  

