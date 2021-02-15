---
title: Метод NextRecordset (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288619"
---
# <a name="nextrecordset-method-ado"></a>Метод NextRecordset (ADO)

**Область применения**: Access 2013, Office 2013
 
Очищает текущий [объект Recordset](recordset-object-ado.md) и возвращает следующий набор **записей** путем надвигания с помощью ряда команд.

## <a name="syntax"></a>Синтаксис

Set *recordset2*  =  *recordset1*. NextRecordset(*RecordsAffected* )

## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **Recordset.** В модели синтаксиса *recordset1* и *recordset2* могут быть одинаковыми **объектами Recordset** или использовать отдельные объекты. При использовании отдельных объектов **Recordset** при сбросе свойства **ActiveConnection** в исходном наборе **recordset** *(recordset1)* после того, как был вызван **NextRecordset,** будет вызвана ошибка.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*RecordsAffected* |Необязательный параметр. **Длинная** переменная, в которую поставщик возвращает количество записей, затронутых текущей операцией.|

> [!NOTE]
> Этот параметр возвращает только количество записей, затронутых операцией; он не возвращает количество записей из заявления select, используемого для создания **recordset.**

## <a name="remarks"></a>Заметки

Используйте метод **NextRecordset** для возврата результатов следующей команды в составном командном заявлении или хранимой процедуре, которая возвращает несколько результатов. Если вы открываете **объект Recordset** на основе составной команды (например, "SELECT \* FROM table1; SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*. Чтобы получить доступ к результатам последующих команд в этом заявлении, вызовите метод **NextRecordset.**

Если имеются дополнительные результаты, а набор **recordset,** содержащий составные утверждения, не отключается или не маршалуется за пределы процесса, метод **NextRecordset** будет продолжать возвращать объекты **Recordset.** Если команда, возвращаемая строкой, выполняется успешно, но не возвращает записей, возвращенный объект **Recordset** будет открытым, но пустым. Проверьте это, проверив, что свойства [BOF](bof-eof-properties-ado.md) и [EOF](bof-eof-properties-ado.md) имеют оба **свойства True.** Если команда, не возвращаемая строкой, выполняется успешно, возвращенный объект **Recordset** будет закрыт, что можно проверить, протестив свойство [State](state-property-ado.md) в **наборе recordset.** Если результатов больше нет, *для набора записей* будет установлено *"Nothing" (Ничего).*

Метод **NextRecordset** не доступен для отключенного объекта **Recordset,** в котором для [ActiveConnection](activeconnection-property-ado.md) установлено **"Nothing"** (в Microsoft Visual Basic) или NULL (на других языках).

Если редактирование идет в режиме немедленного обновления, вызов метода **NextRecordset** создает ошибку; сначала [вызовите метод Update](update-method-ado.md) [или CancelUpdate.](cancelupdate-method-ado.md)

Чтобы передать параметры для более чем одной команды в составном заявлении, заполнив коллекцию [Parameters](parameters-collection-ado.md) или передав массив с помощью исходного вызова **Open** или **Execute,** параметры должны быть в том же порядке в коллекции или массиве, что и соответствующие команды в серии команд. Перед чтением значений выходных параметров необходимо завершить чтение всех результатов.

Поставщик OLE DB определяет, когда выполняется каждая команда в составном операторе. Поставщик [Microsoft OLE DB для SQL Server,](microsoft-ole-db-provider-for-sql-server.md)например, выполняет все команды в пакете после получения составного оператора. Итоги **наборов записей** просто возвращаются при вызове **NextRecordset.**

Однако другие поставщики могут выполнять следующую команду в операторе только после того, как будет вызван NextRecordset. Для этих поставщиков, если вы явно закрываете объект **Recordset** перед пошаговой выполнением всего оператора команды, ADO никогда не выполняет оставшиеся команды.

