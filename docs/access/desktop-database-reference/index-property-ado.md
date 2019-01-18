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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709105"
---
# <a name="index-property-ado"></a>Свойство Index (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает имя индекса в настоящее время фактически для объекта [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, которое является именем индекса.

## <a name="remarks"></a>Замечания

Индекс с именем, свойство **Index** необходимо ранее объявленные в базовой таблице объекта **набора записей** . То есть, индекса необходимо объявлены программными средствами как объект ADOX [индекса](index-object-adox.md) или создания базовой таблицы.

Ошибка времени выполнения возникает, если индекс не может быть задано. Свойство **Index** не могут задаваться:

  - В обработчик событий [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) или **RecordsetChangeComplete** .

  - Если **записей** по-прежнему выполняет операцию (который устанавливается с помощью свойства [State](state-property-ado.md) ).

  - Если установлен фильтр **набора записей** с помощью свойства [фильтра](filter-property-ado.md) .

Свойство **Index** можно задать успешно всегда при закрытии **набора записей** , но не будет открываться **записей** или индекс не будет использоваться, если основной поставщик поддерживает индексы.

Если можно задать индекса, может измениться текущей позиции строки. Это приведет к обновления свойство [AbsolutePosition](absoluteposition-property-ado.md) и созданием **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md)и [MoveComplete](willmove-and-movecomplete-events-ado.md) события.

Если индекс можно задать, является ли данное свойство [LockType для](locktype-property-ado.md) **adLockPessimistic** или **adLockOptimistic**неявных [UpdateBatch](updatebatch-method-ado.md) операция выполняется. Это освобождает текущий и затронутых группы. Выпущен любой существующий фильтр и текущей позиции строки изменяется в первую строку упорядоченный **набор записей**.

Свойство **Index** используется в сочетании с методом [поиска](seek-method-ado.md) . Если базовый поставщик не поддерживает свойство **Index** и, следовательно, метод **Seek** , рекомендуется использовать метод [поиска](find-method-ado.md) . Определите, поддерживает ли объект **набора записей** индексов с помощью метода [поддерживает](supports-method-ado.md)**(adIndex)** .

Встроенные свойства **Index** не связанные с динамическое свойство [оптимизировать](optimize-property-dynamic-ado.md) несмотря на то, что они оба работают со индексов.

