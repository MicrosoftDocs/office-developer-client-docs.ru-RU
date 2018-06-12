---
title: О таблице асинхронной операции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 99bff153d4ce4bac3f85e0ed0feeaffafa6bf3f6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807972"
---
# <a name="about-asynchronous-table-operations"></a>О таблице асинхронной операции
 
**Применимо к**: Outlook 
  
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

