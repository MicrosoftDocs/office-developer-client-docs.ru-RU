---
title: Connection.Exeметод (DAO)
TOCTitle: Execute Method
ms:assetid: d6140d4e-fa14-6455-525e-49d8aab3dff7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835040(v=office.15)
ms:contentKeyID: 48547978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8140dbe9bc0c68d467c011d77bc0c00cec7ad560
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295914"
---
# <a name="connectionexecute-method-dao"></a>Connection.Exeметод (DAO)

**Область применения**: Access 2013, Office 2013

Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.

## <a name="syntax"></a>Синтаксис

*выражение* .Execute(***Query***, ***Options***)

*выражение*: переменная, представляющая объект **Connection**.

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
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Query</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка,</strong> которая является SQL или <strong>свойством Name</strong> объекта <strong>QueryDef.</strong></p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа или сочетание констант, определяющий характеристики целостности данных запроса, как указано в Параметры.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Можно использовать следующие константы **[RecordsetOptionEnum](recordsetoptionenum-enumeration-dao.md)** для параметров.

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
<td><p>Отказывает в разрешении на запись другим пользователям (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInconsistent</strong></p></td>
<td><p>(По умолчанию) Выполняет несогласованные обновления (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbConsistent</strong></p></td>
<td><p>Выполняет согласованные обновления (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSQLPassThrough</strong></p></td>
<td><p>Выполняет SQL-запрос к серверу. При установке этого параметра инструкция SQL передается в базу данных ODBC для обработки (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFailOnError</strong></p></td>
<td><p>Выполняет откат обновлений, если возникает ошибка (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSeeChanges</strong></p></td>
<td><p>Создает ошибку во время выполнения, если другой пользователь пытается изменить данные, которые вы редактируете (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Выполняет запрос асинхронно (только для объектов ODBCDirect Connection и QueryDef).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbExecDirect</strong></p></td>
<td><p>Выполняет инструкцию, не вызывая перед этим функцию API ODBC SQLPrepare (только для объектов ODBCDirect Connection и QueryDef).</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.

> [!NOTE]
> Константы **dbConsistent** и **dbInconsistent** являются взаимоисключающими. В том или ином экземпляре **OpenRecordset** можно использовать любую из них, но не обе. Одновременное использование **dbConsistent** и **dbInconsistent** вызывает ошибку.

Метод **Execute** допустим только для запросов на изменение. Если вы используете метод **Execute** с другим типом запроса, возникает ошибка. Так как запрос на изменение не возвращает записи, метод **Execute** не возвращает объект **Recordset**. (Выполнение запроса SQL к серверу в рабочей области ODBCDirect не вызывает ошибку, если не возвращается объект **Recordset**.)

Свойство **RecordsAffected** объекта **Connection**, **Database** или **QueryDef** используется для определения числа записей, затронутых самым последним вызовом метода **Execute**. Например, **RecordsAffected** содержит число записей, удаленных, обновленных или вставленных при выполнении запроса на изменение. Если метод **Execute** используется для выполнения запроса, в качестве значения свойства **RecordsAffected** объекта **QueryDef** устанавливается число затронутых записей.

Когда в рабочей области Microsoft Access указана синтаксически правильная инструкция SQL и имеются соответствующие разрешения, метод **Execute** не приводит к сбою, даже если не удается изменить или удалить ни одну строку. Поэтому всегда используйте параметр **dbFailOnError** при применении метода **Execute** для обновления или удаления запроса. Этот параметр создает ошибку во время выполнения и откатывает все успешно выполненные изменения, если какие-либо затронутые записи заблокированы и не могут быть обновлены или удалены.

В более ранних версиях ядра СУБД Microsoft Jet инструкции SQL автоматически внедрялись в неявные транзакции. Если часть выполненной инструкции с параметром **dbFailOnError** приводила к сбою, выполнялся откат всей инструкции. Для повышения производительности эти неявные транзакции были удалены начиная с версии 3.5. При обновлении более ранних версий кода DAO рассмотрите возможность использования явных транзакций с инструкциями **Execute**.

Чтобы добиться оптимальной производительности в рабочей области Microsoft Access, особенно в многопользовательской среде, вложите метод **Execute** внутрь транзакции. Используйте метод **BeginTrans** для текущего объекта **Workspace**, затем примените метод **Execute** и завершите транзакцию с помощью метода **CommitTrans** для объекта **Workspace**. Это сохранит изменения на диске и освободит любые блокировки, установленные во время выполнения запроса.

