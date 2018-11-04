---
title: Метод Connection.Execute (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d95b33531f32ebc3524737c3322c92838518b97f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949539"
---
# <a name="connectionexecute-method-dao"></a>Метод Connection.Execute (DAO)

**Применимо к**: Access 2013, Office 2013

Запуск запроса или выполняет инструкции SQL на указанный объект.

## <a name="syntax"></a>Синтаксис

*выражение* . Выполнение (***запроса***, ***Параметры***)

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Query</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p><strong>Строка</strong> , которая является значение свойства <strong>Name</strong> объекта <strong>QueryDef</strong> или инструкции SQL.</p></td>
</tr>
<tr class="even">
<td><p><em>Варианты</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, который определяет характеристики целостности данных запроса, как указано в настройки.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** можно использовать для доступа к параметрам.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDenyWrite</strong></p></td>
<td><p>Запрещает разрешение на запись другим пользователям (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(По умолчанию) Выполняет несогласованных обновлений (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Выполняет согласованности обновлений (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Выполняет запрос к серверу. Если этот параметр передает инструкции SQL к базе данных ODBC для обработки (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Откат обновления при возникновении ошибки (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Создает ошибку времени выполнения, если другой пользователь изменение данных, редактировании (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Выполняет асинхронный запрос (только объекты технология ODBCDirect подключения и QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Выполняет оператор без первого вызова функции SQLPrepare ODBC API (только объекты технология ODBCDirect подключения и QueryDef).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.

> [!NOTE]
> Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими. Можно использовать одно или другое, но не оба в экземпляре **OpenRecordset**. С помощью **dbConsistent** и **dbInconsistent** приводит к ошибке.

Метод **Execute** действителен только для запросов. Если вы используете **Execute** с запрос другого типа, возникает ошибка. Поскольку запрос не возвращает все записи, **выполнение** не возвращает **набор записей**. (Выполнение запроса к серверу в рабочей области технология ODBCDirect не возвращает ошибку при **записей** не возвращаются.)

Используйте свойство **RecordsAffected** объекта **подключения**, **базы данных**или **QueryDef** для определения количества записей, влияет на последнюю метод **Execute** . Например **RecordsAffected** содержит число записей удален, обновляется или вставляется при выполнении запроса. При использовании метода **Execute** для выполнения запроса, свойство **RecordsAffected** объекта **QueryDef** присваивается количество записей.

В рабочей области Microsoft Access, если предоставить синтаксически правильные инструкции SQL и имеют соответствующие разрешения метода **Execute** не ошибка — даже в том случае, если не одной строки можно изменить или удалить. Таким образом всегда используйте параметр **dbFailOnError** , при использовании метода **Execute** для запуска и обновления или удаления запроса. Этот параметр, возникает ошибка времени выполнения и выполняет откат всех изменений успешно Если никакой из записей влияет на блокируется и не может быть обновлении или удалении.

В более ранних версиях ядра базы данных Microsoft Jet SQL операторы автоматически были внедрены в неявные транзакции. Если не удалось выполнить инструкции, с **dbFailOnError** , всей оператор будет выполнен откат. В целях повышения производительности эти неявные транзакции были удалены, начиная с версии 3.5. При обновлении старых кода DAO, необходимо принять во внимание использование явных транзакций вокруг **выполнение** инструкций.

Для достижения наилучшей производительности в рабочую область для Microsoft Access, особенно в многопользовательской среде вложить метода **Execute** внутри транзакции. Используйте метод **BeginTrans** на текущий объект **рабочей области** , а затем используйте метод **Execute** и завершения транзакции с помощью метода **CommitTrans** в **рабочей области**. Это сохраняет изменения на диске и освобождает любые блокировки во время выполнения запроса.

