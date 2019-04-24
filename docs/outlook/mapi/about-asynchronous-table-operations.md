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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329023"
---
# <a name="about-asynchronous-table-operations"></a>Сведения об асинхронных операциях с таблицами
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Интерфейс **IMAPITable** включает три метода, которые работают асинхронно и три метода для управления асинхронной операцией. В следующей таблице перечислены эти методы: 
  
|**Асинхронная операция**|**Асинхронный метод управления**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Получение сведений о состоянии типа таблицы и текущей операции**
  
- Вызов [IMAPITable::/Status](imapitable-getstatus.md). С помощью параметра "- **Status**" пользователь таблицы может определить, является ли таблица статической или динамической, если операция выполняется или выполнена, и если при завершении операции возникла ошибка. Например, если клиенту требуется отменить операцию сортировки, так как он занимает слишком много времени, клиент может сначала вызвать метод "- **Status** ", чтобы определить, обрабатывается ли в настоящее время операция сортировки. Затем клиент может позвонить на вызов [IMAPITable:: Abort](imapitable-abort.md) , чтобы остановить его. 
    
**Приостановка действия до завершения асинхронной задачи**
  
- Вызов [IMAPITable:: ваитфоркомплетион](imapitable-waitforcompletion.md). Вызов **ваитфоркомплетион** позволяет выполнить задачу без прерывания. 
    
## <a name="see-also"></a>См. также

- [Таблицы MAPI](mapi-tables.md)

