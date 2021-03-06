---
title: Настройка позиции таблицы с закладки
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422462"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Настройка позиции таблицы с закладки

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Закладки — это ресурс, который указывает определенное расположение в таблице. Установка закладки позволяет вернуться в позицию в более позднее время, что позволяет значительно повысить производительность операций таблицы. MAPI определяет три стандартные закладки: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Указывает на текущую строку в таблице.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Указывает на первую строку в таблице.  <br/> |
|BOOKMARK_END  <br/> |Указывает на последнюю строку в таблице.  <br/> |
   
Для поддержки этих стандартных закладок необходимы те, кто реализует таблицы, а также могут поддерживать других. Однако, поскольку закладки — это ресурсы, а ресурсы ограничены, пользователям закладки следует освободить их как можно скорее. 
  
 **Настройка закладки в текущей позиции таблицы**
  
- Вызов [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Иногда будет недостаточно памяти для выделения новой закладки, в результате чего **CreateBookmark** возвращает значение MAPI_E_UNABLE_TO_COMPLETE ошибки. 
    
 **Чтобы освободить закладки**
  
- Вызов [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **Перемещение курсора в закладки**
  
- Вызов [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** устанавливает новое значение для BOOKMARK_CURRENT позиции. **SeekRow** можно использовать, например, для позиции таблицы десять строк из текущей позиции или для начала. Клиенты или поставщики услуг могут искать текущее, начало или конец таблицы или любую другую позицию, связанную с заранее заранее закладки. Они могут перемещаться в направлении вперед или назад и ограничить операцию заданным количеством строк. Как правило, звонящем следует искать не более 50 строк с **SeekRow;** [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) следует использовать с большим количеством строк. 
    
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

