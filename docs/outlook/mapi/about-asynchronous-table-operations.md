---
title: О таблице асинхронной операции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569423"
---
# <a name="about-asynchronous-table-operations"></a>О таблице асинхронной операции
 
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Интерфейс **IMAPITable** включает в себя три метода, которые используются асинхронно и три методы для управления асинхронной операции. В следующей таблице приведены следующие методы: 
  
|**Асинхронной операции**|**Метод асинхронного управления**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Для получения сведений о типе и текущей операции таблицы**
  
- Вызов [IMAPITable::GetStatus](imapitable-getstatus.md). **GetStatus**пользователя в таблице определить ли таблицы статических или динамических, если находится в стадии разработки или завершения операции, и если произошла ошибка завершения операции. Например если это клиент должен отменить операцию сортировки, так как она выполняется слишком много времени, клиента можно вызвать **GetStatus** , чтобы определить, на самом деле операции сортировки в настоящее время обрабатывает ли. Затем клиент может вызывать [IMAPITable::Abort](imapitable-abort.md) , чтобы остановить его. 
    
**Для приостановки действия до завершения асинхронной задачи**
  
- Вызов [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). Вызов **WaitForCompletion** позволяет завершение без прерывания задачи. 
    
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

