---
title: Delete Method (ADO Recordset)
TOCTitle: Delete Method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 118cc56bf33812819dd34089ac97c72259228f4c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482155"
---
# <a name="delete-method-ado-recordset"></a>Delete Method (ADO Recordset)


**Применимо к**: Access 2013 | Office 2013



Удаление текущей записи или группы записей.

## <a name="syntax"></a>Синтаксис

*набор записей*. Удаление *AffectRecords*

## <a name="parameters"></a>Параметры

  - *AffectRecords*

  - Метод **Delete** повлияет от [AffectEnum](affectenum.md) значение, определяющее число записей. Значение по умолчанию — **adAffectCurrent**.


> [!NOTE]
> <P><STRONG>adAffectAll</STRONG> и <STRONG>adAffectAllChapters</STRONG> не допустимый аргументы, которые нужно <STRONG>Удалить</STRONG>.</P>



## <a name="remarks"></a>Замечания

С помощью метода **Delete** помечает текущую запись или группу из записей в объекте [набора записей](recordset-object-ado.md) для удаления. Если объект **набора записей** не позволяет удаление записи, возникает ошибка. Если вы используете режим немедленное обновление, удаление происходит в базе данных немедленно. Если запись не может успешно удалены (из-за нарушения целостности базы данных, например), запись будет оставаться в режиме редактирования после вызова **обновления**. Это означает, что необходимо отменить обновление с [CancelUpdate](cancelupdate-method-ado.md) перед перемещением текущей записи (например, с помощью [Закрыть](close-method-ado.md), [Перемещение](move-method-ado.md)или [NextRecordset](nextrecordset-method-ado.md)).

Если вы используете режим пакетного обновления, записи помечаются для удаления из кэша и фактическое удаление происходит при вызове метода [UpdateBatch](updatebatch-method-ado.md) . (Используйте свойство [фильтра](filter-property-ado.md) для просмотра удаленных записей).

Получение значений полей из удаленной записи приводит к ошибке. После удаления текущей записи удаленной записи остается текущей до перехода к другой записи. Один раз удалении от удаленной записи, он больше не доступен.

Если вложить удалений в транзакции, вы можете восстанавливать удаленные записи с помощью метода [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) . Если вы используете режим пакетного обновления, можно отменить ожидающие удаления или группой ожидающих удалений с помощью метода [CancelBatch](cancelbatch-method-ado.md) .

Если происходит сбой попытки для удаления записей из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы. Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.

Если свойство [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) установлено и **записей** производится в результате выполнения операции СОЕДИНЕНИЯ на несколько таблиц, то метод **Delete** только удаляет строки в таблице с именем в свойстве [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .
