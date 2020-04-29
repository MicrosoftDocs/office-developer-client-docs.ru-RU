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
  
Знание того, как и когда следует распределять и освобождать память, является важной частью программирования с использованием MAPI. MAPI предоставляет функции и макросы, которые может использовать клиент или поставщик услуг для согласованного управления памятью. Существуют следующие три функции:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Когда клиенты и поставщики услуг используют эти функции, выдается вопрос о том, что "владеет" (то есть, как выпустить, что устраняет определенный блок памяти). Клиент, вызывающий метод поставщика услуг, не должен передавать буфер достаточно большим для хранения возвращаемого значения любого размера. Поставщик услуг может просто выделить соответствующий объем памяти с помощью **мапиаллокатебуффер** и, при необходимости, **мапиаллокатеморе**, и клиент может позже отпустить его, используя **мапифрибуффер**, не зависящее от поставщика услуг. 
  
Макросы памяти используются для выделения структур или массивов структуры определенного размера. Клиенты и поставщики услуг должны использовать эти макросы вместо того, чтобы выделить память вручную. Например, если клиенту требуется выполнить обработку разрешения имен для списка получателей с тремя записями, макрос **сизедадрлист** можно использовать для создания структуры **ADRLIST** , которая передается в **IAddrBook:: ресолвенаме** с правильным числом членов **адрентри** . Все макросы памяти определены в MAPIDEFS. H файл заголовка. Эти макросы: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI также поддерживает [Использование интерфейса COM](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) для управления памятью. Поставщику **услуг во время** инициализации получится указатель интерфейса исходящей информации, а также можно получить один из них с помощью функции [мапижетдефаултмаллок](mapigetdefaultmalloc.md) . Основное преимущество использования методов **unalloc** для управления памятью через функции MAPI заключается в том, что методы COM могут перераспределить существующий буфер. Функции памяти MAPI не поддерживают перераспределение. 
  

