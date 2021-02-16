---
title: Сведения об асинхронных операциях с таблицами
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439571"
---
# <a name="about-asynchronous-table-operations"></a>Сведения об асинхронных операциях с таблицами
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Интерфейс **IMAPITable** включает три метода, которые работают асинхронно, и три метода управления асинхронной операцией. В следующей таблице перечислены следующие методы: 
  
|**Асинхронная операция**|**Метод асинхронного управления**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Извлечение сведений о состоянии типа таблицы и текущей операции**
  
- Вызов [IMAPITable::GetStatus](imapitable-getstatus.md). С **помощью GetStatus** пользователь таблицы может определить, является ли таблица статической или динамической, находится ли операция в процессе выполнения или завершена, а также произошла ли ошибка в результате выполненной операции. Например, если клиенту необходимо отменить операцию сортировки, так как она требует слишком много времени, клиент может сначала вызвать **GetStatus,** чтобы определить, действительно ли операция сортировки в настоящее время обрабатывается. Затем клиент может вызвать [IMAPITable::Abort,](imapitable-abort.md) чтобы остановить его. 
    
**Приостановка действия до завершения асинхронной задачи**
  
- Вызов [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). Вызов **WaitForCompletion** позволяет выполнить задачу без прерывания. 
    
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

