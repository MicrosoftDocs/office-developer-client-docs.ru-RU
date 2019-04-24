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

Указывает имя индекса, действующего в текущий момент для объекта [Recordset](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает **строковое** значение, представляющее собой имя индекса.

## <a name="remarks"></a>Замечания

Индекс, указанный в свойстве **index** , должен быть ранее объявлен в базовой таблице базового объекта **Recordset** . Таким образом, индекс должен быть объявлен программным способом либо как объект [индекса](index-object-adox.md) ADOX, либо при создании базовой таблицы.

Если не удается задать индекс, произойдет ошибка времени выполнения. Не удается задать свойство **index** :

  - В обработчике событий [события willchangerecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) или **RecordsetChangeComplete** .

  - Если **набор записей** по-прежнему выполняет операцию (которая может быть определена свойством [State](state-property-ado.md) ).

  - Если в наборе **записей** задан фильтр со свойством [Filter](filter-property-ado.md) .

Свойство **index** всегда можно задать, если **набор записей** закрыт, но объект **Recordset** не будет открыт успешно, или индекс не будет использоваться, если базовый поставщик не поддерживает индексы.

Если индекс можно задать, положение текущей строки может измениться. Это приведет к обновлению свойства [AbsolutePosition](absoluteposition-property-ado.md) и созданию событий **события willchangerecordset**, **RecordsetChangeComplete**, [события WillMove](willmove-and-movecomplete-events-ado.md)и [MoveComplete](willmove-and-movecomplete-events-ado.md) .

Если индекс можно задать и свойство [LockType](locktype-property-ado.md) равно **адлоккпессимистик** или **адлоккоптимистик**, выполняется неявная операция [UpdateBatch](updatebatch-method-ado.md) . В результате этого выпускаются текущие и затронутые группы. Будет выпущен любой существующий фильтр, а текущая позиция строки изменится на первую строку переупорядоченного **набора записей**.

Свойство **index** используется совместно с методом [Seek](seek-method-ado.md) . Если базовый поставщик не поддерживает свойство **index** и, соответственно, метод **Seek** , рекомендуется использовать метод [Find](find-method-ado.md) . Определите, поддерживает ли объект **Recordset** индексацию с [](supports-method-ado.md)помощью метода support **(адиндекс)** .

Встроенное свойство **индекса** не связано с динамическим свойством [optimize](optimize-property-dynamic-ado.md) , несмотря на то, что они оба работают с индексами.

