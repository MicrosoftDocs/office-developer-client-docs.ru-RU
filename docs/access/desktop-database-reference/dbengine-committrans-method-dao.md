---
title: Метод DBEngine.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75918ac4da32020214d9e58d866c5def169eede3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294389"
---
# <a name="dbenginecommittrans-method-dao"></a>Метод DBEngine.CommitTrans (DAO)


**Область применения**: Access 2013, Office 2013

Завершает текущую транзакцию и сохраняет изменения.

## <a name="syntax"></a>Синтаксис

*выражения* . ***CommitTrans(Option)***

*expression*: переменная, представляющая объект **DBEngine**.

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
<td><p><em>Option</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>В рабочей области Microsoft Access можно включить константу <strong>dbForceOSFlush</strong> с <strong>CommitTrans.</strong> Это заставляет двигатель базы данных немедленно смывать все обновления на диск, а не временно кэшывать их. Не используя этот параметр, пользователь может получить контроль сразу после вызова программы приложения <strong>CommitTrans,</strong>отключить компьютер и не иметь данные, написанные на диск. Использование этого параметра может повлиять на производительность приложения, но оно полезно в ситуациях, когда компьютер можно отключить перед тем, как кэшировали обновления, сохраненные на диске.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Методы транзакций **BeginTrans,** **CommitTrans** и **Rollback** управляют обработкой транзакций во время сеанса, определенного объектом **Рабочей** области. Эти методы используются с объектом **Workspace,** когда необходимо рассматривать ряд изменений, внесенных в базы данных в сеансе, как одно целое.

Как правило, транзакции используются для поддержания целостности данных, когда необходимо обновлять записи в двух или более таблицах и обеспечивать, чтобы изменения были завершены (зафиксированы) во всех таблицах или вообще нет (откат). Например, при переводе денег с одной учетной записи на другую можно вычесть сумму из одной и добавить ее в другую. Если обновление не удается, учетные записи перестают балансировать. Используйте метод **BeginTrans** перед обновлением первой записи, а затем, если любое последующее обновление сбой, вы можете использовать метод **отката,** чтобы отменить все обновления. Используйте метод **CommitTrans** после успешного обновления последней записи.

> [!NOTE]
> В одном **объекте Workspace** транзакции всегда являются глобальными для **рабочей** области и не ограничиваются только одним объектом **Подключения** или **Базы данных.** Если вы выполняете операции по более чем одному подключению или базе данных в транзакции **Workspace,** решение транзакции (то есть с помощью метода **CommitTrans** или **Rollback)** влияет на все операции на всех подключениях и базах данных в этом рабочем пространстве.

После использования **CommitTrans** нельзя отменить изменения, внесенные во время этой транзакции, если транзакция не будет вложена в другую транзакцию, которая сама откатится. При вложении транзакций необходимо решить текущую транзакцию, прежде чем разрешить транзакцию на более высоком уровне вложения.

Если вы хотите иметь одновременные транзакции с перекрывающимися, не вложенными областьми, можно создать дополнительные объекты **Workspace,** чтобы содержать одновременные транзакции.

Если вы закрываете **объект Workspace** без разрешения каких-либо ожидающих транзакций, транзакции автоматически откатываются обратно.

Если вы используете метод **CommitTrans или** **Rollback** без использования метода **BeginTrans,** возникает ошибка.

Некоторые базы данных ISAM, используемые в рабочей области Microsoft Access, могут не поддерживать транзакции, в этом случае свойство **Transactions** объекта **Database** или **объекта Recordset** является **false**. Чтобы убедиться, что база данных поддерживает транзакции, перед использованием метода **BeginTrans** проверьте значение свойства **Transactions** объекта **Database.** Если вы используете объект **Recordset** на основе более чем одной базы данных, проверьте свойство **Transactions** объекта **Recordset.** Если набор **recordset** полностью основан на таблицах баз данных Microsoft Access, всегда можно использовать транзакции. **Однако объекты recordset** на основе таблиц, созданных другими продуктами базы данных, могут не поддерживать транзакции. Например, вы не можете использовать транзакции в **наборе recordset** на основе таблицы Paradox. В этом случае свойство **Transactions** является **false**. Если **база данных** или **набор записей** не поддерживают транзакции, методы игнорируются и ошибки не происходят.

Вы не можете вложенные транзакции, если вы имеете доступ к источникам данных ODBC с помощью двигателя базы данных Microsoft Access.

В рабочей области ODBC при использовании **CommitTrans** курсор может перестать быть допустимым. Используйте метод **Requery** для просмотра изменений в **Наборе записей** или закрытия и повторного **открытия наборов записей.**


> [!NOTE]
> - Вы часто можете повысить производительность приложения, разбивая операции, которые требуют доступа к диску в блоки транзакций. Это буферит операции и может значительно сократить количество случаев доступа к диску.
> - В рабочей области Microsoft Access транзакции регистрируются в файле, который хранится в каталоге, указанном переменной среды TEMP на рабочей станции. Если файл журнала транзакций исчерпает доступное хранилище на диске TEMP, двигатель базы данных вызывает ошибку во время запуска. На этом этапе при использовании **CommitTrans** совершается неопределяемая численность операций, но остальные незавершенные операции теряются, и операция должна быть перезапущена. Метод **отката** освобождает журнал транзакций и откатит все операции в транзакции.
> - Закрытие клона **Recordset в** ожидаемой транзакции приведет к неявной операции **отката.**


