---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809609"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**Относится к**: Outlook 
  
Обеспечивает вспомогательные методы для работы с таблицами. MAPI предоставляет таблицы данных объектов или объектов, которые реализуют **ITableData** для поставщиков услуг проводите обслуживание в таблице. Чтобы получить объект данных в таблице, поставщиков услуг вызовите функцию [CreateTable](createtable.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Предоставляемые:  <br/> |Объекты данных в таблице  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPITableData  <br/> |
|Тип указателя:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |Создание нового представления таблицы, возвращает указатель на реализацию [IMAPITable](imapitableiunknown.md) .  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |Добавление новой строки в таблице, возможно заменить существующую строку.  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |Удаляет строку в таблице.  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |Получает строку таблицы.  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |Получает строку на основе его расположения в таблице.  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |Отправляет уведомления для строки в таблице.  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |Вставляет строку в таблице.  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |Вставка нескольких строк таблицы, возможно замена существующих строк.  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |Удаление нескольких строк таблицы.  <br/> |
   
## <a name="remarks"></a>Замечания

Реализация интерфейса MAPI **ITableData** работает с таблицами, удерживая любые связанные ограничений и все данные в память, что подходит для использования с очень большой таблицы. Сложные операции, такие как категоризации и больших ограничения не поддерживается. 
  
Объекты данных в таблице идентификации строк с помощью столбца индекса, свойство, которое гарантированно имеет уникальное значение для каждой строки. Большинство поставщиков услуг используйте свойство **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) в столбце индекса. Свойства, которые имеют несколько значений нельзя использовать в качестве столбца индекса.
  
Объекты данных в таблице создания одного уведомления независимо от количества строк, затронутых изменения или удаления. Если в целевой строке в рамках одной операции не существует, добавлении строки.
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

