---
title: Модель COM и MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cca4c70d-b73a-4834-80b5-9cb5889f63cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a91ab8497a690fd4b99f76274d0213284253fd06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334470"
---
# <a name="component-object-model-and-mapi"></a>Модель COM и MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Документация Windows SDK включает всестороннее обсуждение правил реализации объектов, которые соответствуют объектной модели компонентов (COM). В этих правилах решается вопрос о том, как сделать следующее:
  
- Проектирование интерфейсов и объектов.
    
- Реализация [интерфейса IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) 
    
- Управление памятью.
    
- Обработка подсчета ссылок.
    
- Реализация объектов с резьбой по квартирам.
    
Хотя все объекты MAPI считаются com-базами, так как они реализуют интерфейсы, унаследованные от [IUnknown,](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx)MAPI в некоторых ситуациях отклоняется от стандартных правил COM. Это отклонение позволяет разработчикам более гибко использовать их реализацию. Например, интерфейс MAPI, как и любой интерфейс COM, описывает контракт между реализации и вызываемой. После создания и публикации интерфейса его определение не может и не меняется. MAPI не отклоняться от этого описания, но это несколько расслабляет описание. Реализация может не реализовывать определенные методы, возвращая одному из следующих значений ошибки вызываемого: 
  
- MAPI_E_NO_SUPPORT
    
- MAPI_E_TOO_COMPLEX
    
- MAPI_E_BAD_CHARWIDTH
    
- MAPI_E_TYPE_NO_SUPPORT
    
Другие отклонения от стандартных правил COM описаны в следующей таблице.
  
|**Правило программирования COM**|**Вариант MAPI**|
|:-----|:-----|
|Все параметры строки в методах интерфейса должны быть Юникодом.  <br/> |Интерфейсы MAPI определяются для разрешения параметров строки Unicode или ANSI. Многие методы, которые имеют параметр строки, также имеют **параметр ulFlags;** ширина параметра строки указывается значением флага MAPI_UNICODE **в ulFlags**. Некоторые интерфейсы MAPI не поддерживают Юникод и возвращают MAPI_E_BAD_CHARWIDTH при MAPI_UNICODE флага.  <br/> |
|Все методы интерфейса должны иметь возвращаемого типа HRESULT.  <br/> |MAPI имеет по крайней мере один метод, который возвращает значение, не относящеся к HRESULT: [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md).  <br/> |
|Звонители и реализутели должны выделять и бесплатно выделять память для параметров интерфейса с помощью стандартных распределителей задач COM.  <br/> |Все методы MAPI используют связанные алокаторы [MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) для управления памятью для параметров интерфейса. Все реализации интерфейсов MAPI, определенных OLE, например [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)используют стандартные ком-решения задач.  <br/> |
|Все параметры указателя на выходе должны быть явно заданы NULL при сбой метода.  <br/> |Интерфейсы MAPI требуют, чтобы параметры указателей либо были заданы nULL, либо оставались неизменными при сбой метода. Все реализации интерфейсов MAPI, определенные OLE, явно определяют параметры NULL при сбое.  <br/> |
|Реализация агрегируемых объектов по мере возможности.  <br/> |Интерфейсы MAPI не являются агрегируемыми.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Обзор объектов и интерфейсов MAPI](mapi-object-and-interface-overview.md)

