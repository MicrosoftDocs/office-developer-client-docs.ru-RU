---
title: Свойство Index (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291708"
---
# <a name="index-property-ado"></a>Свойство Index (ADO)


**Область применения**: Access 2013, Office 2013

Указывает имя индекса, который в настоящее время действует для [объекта Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает или возвращает **значение String,** которое является именем индекса.

## <a name="remarks"></a>Примечания

Индекс, названный **свойством Index,** должен быть объявлен ранее в базовой таблице, в основе которого находится объект **Recordset.** То есть индекс должен быть объявлен программным путем либо [](index-object-adox.md) как объект индекса ADOX, либо при создания базовой таблицы.

Ошибка при запуске произойдет, если не удается установить индекс. Свойство **Index** не может быть установлено:

  - В [обработнике событий WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) или **RecordsetChangeComplete.**

  - Если **в Recordset** по-прежнему выполняется операция (которая может быть определена государственным [свойством).](state-property-ado.md)

  - Если в наборе **Recordset** установлен фильтр с [свойством Filter.](filter-property-ado.md)

Свойство **Index** всегда можно успешно зафиксировать, если набор **recordset** закрыт, но **recordset** не откроется успешно, или индекс не будет использовать, если поставщик не поддерживает индексы.

Если можно установить индекс, текущая позиция строки может измениться. Это приведет к обновлению свойства [AbsolutePosition](absoluteposition-property-ado.md) и поколению **событий WillChangeRecordset,** **RecordsetChangeComplete,** WillMove и [MoveComplete.](willmove-and-movecomplete-events-ado.md) [](willmove-and-movecomplete-events-ado.md)

Если можно установить индекс и свойство [LockType](locktype-property-ado.md) является **adLockPessimistic** или **adLockOptimistic,** то выполняется неявная операция [UpdateBatch.](updatebatch-method-ado.md) Это освобождает текущие и затронутые группы. Любой существующий фильтр освобожден, а текущая позиция строки изменена на первую строку переустановленного **Набор записей.**

Свойство **Index** используется совместно с методом [Seek.](seek-method-ado.md) Если поставщик не поддерживает свойство **Index** и, следовательно, метод **Seek,** подумайте об использовании метода [Find.](find-method-ado.md) Определите, поддерживает ли объект **Recordset** индексы методом [Supports](supports-method-ado.md)**(adIndex).**

Встроенное свойство **Index** не связано с динамическим свойством Оптимизируйте, хотя оба они касаются индексов. [](optimize-property-dynamic-ado.md)

