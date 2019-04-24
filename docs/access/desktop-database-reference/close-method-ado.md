---
title: 'Метод Close: ActiveX Data Objects (ADO)'
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

ЗаКрывает открытый объект и все зависимые объекты.

## <a name="syntax"></a>Синтаксис

*object*.Close

## <a name="remarks"></a>Замечания

Используйте метод **Close** для закрытия [подключения](connection-object-ado.md), [записи](record-object-ado.md), [набора записей](recordset-object-ado.md)или объекта [Stream](stream-object-ado.md) , чтобы освободить все связанные системные ресурсы. При закрытии объекта его не удаляются из памяти; Вы можете изменить его свойства и открыть позже. Чтобы полностью удалить объект из памяти, присвойте переменной объекта значение *Nothing* (в Visual Basic) после закрытия объекта.

**Connection**

При закрытии объекта **Connection** с помощью метода **Close** также закрываются все активные объекты **Recordset** , связанные с подключением. Объект [Command](command-object-ado.md) , связанный с закрываемым объектом **Connection** , будет оставаться несвязанным, но больше не будет связан с объектом **Connection** ; то есть для свойства [ActiveConnection](activeconnection-property-ado.md) будет задано значение **Nothing**. Кроме того, коллекция [Parameters](parameters-collection-ado.md) объекта **Command** будет очищена от любых параметров, определенных поставщиком.

Позже можно вызвать метод [Open](open-method-ado-connection.md) , чтобы повторно установить подключение к тому же или другому источнику данных. Когда объект **Connection** закрывается, вызов всех методов, которым требуется открытое подключение к источнику данных, приводит к ошибке.

Закрытие объекта **Connection** при наличии открытых объектов **Recordset** в подключении выполняет откат всех ожидающих изменений во всех объектах **Recordset** . Явное закрытие объекта **Connection** (вызов метода **Close** ) во время выполнения транзакции приводит к возникновению ошибки. Если объект **Connection** выходит за пределы области действия в ходе выполнения транзакции, ADO автоматически выполняет откат транзакции.

**Recordset, Record, Stream**

При использовании метода **Close** для закрытия связанных данных **Recordset**, **Record**или **Stream** освобождается и любой монопольный доступ к данным с помощью этого конкретного объекта. Позже можно вызвать метод [Open](open-method-ado-recordset.md) , чтобы повторно открыть объект с теми же или измененными атрибутами.

При закрытии объекта **Recordset** при вызове всех методов, требующих наличия Live курсора, возникает ошибка.

Если редактирование выполняется в режиме немедленного обновления, вызов метода **Close** приводит к возникновению ошибки; Вместо этого сначала вызовите метод [Update](update-method-ado.md) или [CancelUpdate](cancelupdate-method-ado.md) . Если объект **Recordset** закрывается в режиме пакетного обновления, все изменения, выполненные с момента последнего вызова [UpdateBatch](updatebatch-method-ado.md) , теряются.

Если вы используете метод [clone](clone-method-ado.md) для создания копий объекта Open **Recordset** , закрытие исходного объекта или клона не повлияет на другие копии.

