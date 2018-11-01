---
title: Метод CancelBatch (ADO)
TOCTitle: CancelBatch Method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 24444aa40fae38987f1dab284a37239b281ecb58
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886559"
---
# <a name="cancelbatch-method-ado"></a>Метод CancelBatch (ADO)


**Применимо к**: Access 2013, Office 2013


Показано, как отменить ожидающие пакетного обновления.

## <a name="syntax"></a>Синтаксис

*набор записей*. CancelBatch *AffectRecords*

## <a name="parameters"></a>Параметры

  - *AffectRecords*

  - Необязательный параметр. От [AffectEnum](affectenum.md) значение, которое указывает, сколько записей влияет на метод **CancelBatch** .

## <a name="remarks"></a>Замечания

Используйте метод **CancelBatch** для отмены ли ожидающих установки обновлений в [записей](recordset-object-ado.md) в пакетном режиме обновления. Если в режиме немедленное обновление **набора записей** , вызов **CancelBatch** без **adAffectCurrent** приводит к ошибке.

При изменении текущей записи или добавление новой записи при вызове **CancelBatch**ADO сначала вызывает метод [CancelUpdate](cancelupdate-method-ado.md) , чтобы отменить все изменения кэширования. После этого отменяются все ожидающие изменения в **набора записей** .

Это и возможно, что текущей записи будут неопределенной после вызова метода **CancelBatch** , особенно в том случае, если были в процессе добавления новой записи. По этой причине лучше установка в настоящее время записи для заданного расположения в **записей** после вызова **CancelBatch** . Например вызовите метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .

Если не удалось отменить ожидающие обновления из-за конфликта с базовыми данными (например, запись была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы. Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения. Используйте свойство [фильтра](filter-property-ado.md) (**adFilterAffectedRecords**) и свойство [состояние](status-property-ado-recordset.md) для поиска записей с конфликтами.

