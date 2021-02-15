---
title: Close Method — ActiveX Data Objects (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 269a782e85fab1e5dc47cd32f2e2c11306e11470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296313"
---
# <a name="close-method-ado"></a>Метод Close (ADO)


**Область применения**: Access 2013, Office 2013

Закрывает открытый объект и все зависимые объекты.

## <a name="syntax"></a>Синтаксис

*object*.Close

## <a name="remarks"></a>Заметки

Используйте метод **Close,** чтобы закрыть [подключение,](connection-object-ado.md) [запись,](record-object-ado.md)набор записей или объект [Stream,](stream-object-ado.md) чтобы освободить все связанные системные ресурсы. [](recordset-object-ado.md) Закрытие объекта не удаляет его из памяти; вы можете изменить его параметры свойств и открыть его позже. Чтобы полностью исключить объект из памяти, установите для переменной объекта значение *Nothing* (Visual Basic) после закрытия объекта.

**Connection**

Использование метода **Close** для закрытия объекта **Connection** также закрывает все активные объекты **Recordset,** связанные с подключением. Объект [Command,](command-object-ado.md) связанный с закрываемом объектом **Connection,** будет сохраняться, но больше не будет связан с **объектом Connection;** то есть его свойство [ActiveConnection](activeconnection-property-ado.md) будет иметь свойство **Nothing.** Кроме того, **коллекция параметров** объекта [Command](parameters-collection-ado.md) будет очищена от параметров, определенных поставщиком.

Позднее можно вызвать метод [Open,](open-method-ado-connection.md) чтобы повторно установить подключение к одному или другому источнику данных. При **закрытии** объекта Connection вызов любых методов, которые требуют открытого подключения к источнику данных, создает ошибку.

Закрытие объекта **Connection** при открытом объекте **Recordset** в подсети откатит все ожидающих изменений во всех **объектах Recordset.** Явное закрытие объекта **Connection** (вызов метода **Close)** во время выполнения транзакции вызывает ошибку. Если объект **Connection** выходит за пределы области действия во время выполнения транзакции, ADO автоматически откатит транзакцию.

**Recordset, Record, Stream**

Использование метода **Close** для закрытия объекта **Recordset,** **Record** или **Stream** освобождает связанные данные и любой монопольный доступ к данным через этот конкретный объект. Позднее можно вызвать метод [Open,](open-method-ado-recordset.md) чтобы повторно открыть объект с помощью тех же или измененных атрибутов.

При **закрытии** объекта Recordset вызов любых методов, для работы с которые требуются живые курсоры, создает ошибку.

Если редактирование идет в режиме немедленного обновления, вызов метода **Close** создает ошибку; вместо этого сначала вызовите метод [Update](update-method-ado.md) [или CancelUpdate.](cancelupdate-method-ado.md) Если закрыть объект **Recordset** в режиме пакетного обновления, все изменения, внесенные с момента последнего вызова [UpdateBatch,](updatebatch-method-ado.md) будут потеряны.

Если вы используете метод [Clone](clone-method-ado.md) для создания копий открытого объекта **Recordset,** закрытие исходного или клона не влияет ни на какие другие копии.

