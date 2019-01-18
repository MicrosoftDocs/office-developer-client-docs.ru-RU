---
title: Справочник по ошибкам ADO
TOCTitle: ADO error reference
ms:assetid: 21cec161-664a-4c18-4458-8117f4f63845
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248997(v=office.15)
ms:contentKeyID: 48543690
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a7f756af1422588d99fcffe1ae1413422131b70
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717239"
---
# <a name="ado-error-reference"></a>Справочник по ошибкам ADO

**Применимо к**: Access 2013, Office 2013

Константа **ErrorValueEnum** описаны значения ошибка ADO. Полный список эти перечисленные константы, включая значения отображаются [Ошибки ADO B: приложение](appendix-b-ado-errors.md). В этом разделе будет проверить некоторые из наиболее интересных ошибок и описываются некоторые конкретных ситуаций, которые могут вызывать их или с помощью решений для решения проблемы. Перечисленные константы **ErrorValueEnum** и короткий положительное десятичное число.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Число</p></th>
<th><p>Константа ErrorValueEnum</p></th>
<th><p>Описание/возможные причины</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>Не удалось выполнить запрошенную операцию поставщика.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом. Ошибка ввода в инструкции SQL SELECT зачастую причиной этой ошибки. Например ошибочным поля имя или имя таблицы можно создать эту ошибку. Эта ошибка может возникнуть при поля или таблице с именем в операторе SELECT не существует в хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Не удается открыть файл. Было указано имя файла с ошибками, или файл были перемещены, переименованы или удалении. В сети диске временно недоступен или сетевой трафик, препятствующих подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Не удалось прочитать файл. Неправильно указано имя файла, возможно, файл был перемещен или удален или файл может быть поврежден.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Запись в файл не удалось. Закрытием файла и затем попытка записи в него, или файл поврежден. Если файл расположен на сетевого диска, временное состояние сети могут запретить запись сетевого диска.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p><strong>BOF</strong> или <strong>EOF</strong> имеет значение True или текущей запись была удалена. Запрошенная операция требует текущей записи. Предпринята попытка обновить записей с помощью <strong>Поиск</strong> или <strong>Seek</strong> поместите указатель записи к нужной записи. Если запись не найден, <strong>EOF</strong> будет иметь значение True. Эта ошибка могут также создаваться после неудачной <strong>AddNew</strong> или <strong>Удалить</strong> , так как отсутствует текущий запись при сбое эти методы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>Операция не допускается в данном контексте.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>Заданный поставщик отличается от одной уже для использования.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>Объект <strong>подключения</strong> не может быть закрыт явным образом в транзакции. Объект <strong>подключения</strong> или <strong>набора записей</strong> , в настоящее время участвует в транзакции не может быть закрыт. Вызовите <strong>RollbackTrans</strong> или <strong>CommitTrans</strong> перед закрытием объект.</p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>Объект или поставщик не может выполнить запрошенную операцию. Некоторые операции зависят от версии определенного поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>Не удается найти элемента в коллекции, соответствующий запрошенные имя или порядковый номер. Указано неправильное имя поля или таблицы.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>Объект уже присутствует в коллекции. Не удается добавить. Объект нельзя добавить в два раза одного семейства сайтов.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>Объект больше не является допустимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>Приложение использует значение недопустимого типа для текущей операции. Возможно, предоставленные строку операции, требующей потока, например.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>Операция не допускается при закрытии объекта. <strong>Подключение</strong> или <strong>набора записей</strong> был закрыт. Например некоторые другие подпрограммы закрытием глобальный объект. Эта ошибка может запретить, обращаясь к свойству <strong>состояние</strong> перед выполнением операции.</p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>Операция не разрешена, когда объект открыт. Не удается открыть объект, который открыт. Не удается добавить поля open <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>Не удается найти поставщика. Она может быть установлено неправильно. Имя поставщика может быть неправильно указано, указанного поставщика не может быть установлен на компьютере, где выполнение кода или установки может быть поврежден.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>Свойства <strong>ActiveConnection</strong> объекта <strong>набора записей</strong> , который содержит объект <strong>команды</strong> в качестве источника, нельзя изменить. Приложения, попытка назначить новый объект <strong>подключения</strong> <strong>набора записей</strong> , который содержит объект <strong>команды</strong> в качестве источника.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>Объект <strong>параметра</strong> определен неправильно. Несогласованные или неполные сведения отсутствуют.</p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>Подключение не может использоваться для выполнения этой операции. Он является закрытой или недопустимый в данном контексте.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>Невозможно выполнить операцию во время обработки событий. Операция не могут выполняться в обработчик событий, который вызывает событие еще раз. Например методы перемещения не должен вызываться из обработчика событий <strong>WillMove</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>Невозможно выполнить операцию во время выполнения асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>Операция отменена пользователем. Приложение называется <strong>CancelUpdate</strong> или метод <strong>CancelBatch</strong> и текущей операции было прервано.</p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>Не удается выполнить операцию при подключении асинхронно.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>Координирование транзакций является недопустимым или не запущен.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>Невозможно выполнить операцию во время не выполняется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>Параметры безопасности на данном компьютере запрещают доступ к источнику данных в другом домене.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Только для внутреннего использования. Не следует использовать. (Запись был включен для полноты. Эта ошибка не должно быть в вашем коде.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Только для внутреннего использования. Не следует использовать. (Запись в включены для полноты. Эта ошибка не должно быть в вашем коде.)</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>Данные значения конфликтует с ограничения целостности поля. Новое значение для <strong>поля</strong> вызовет повторяющийся ключ. Значение, которое forms одностороннего отношения между двумя записями может оказаться обновляемым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>Имеющихся разрешений недостаточно не позволяет записи в поле. Пользователя, указанного в строке подключения не имеет разрешения, необходимые для записи в <strong>поле</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>Значение данных слишком велик для представления по типу данных поля. Числовое значение, которое слишком велико для требуемого поля была назначена. Например поле короткое целое число присвоено значение "длинное целое".</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Данные значения конфликтует с типом данных или ограничения поля. Хранилище данных имеет ограничения проверок, которые отличаются в зависимости от значения <strong>поля</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>Сбой преобразования, так как значение данных имеет знак, а тип данных поля, используемый поставщиком без знака.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>Невозможно преобразовать значение данных по причине, отличной от несоответствия знака или данных переполнения. Например, для преобразования будет усечено данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>Значение данных не может быть задана или получена так, как тип данных поля неизвестно или должен недостаточно ресурсов для выполнения операции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>Запись не содержит это поле. Указан неправильный поля имя или ссылка на поле не в коллекции <strong>полей</strong> текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>Исходный URL-адрес или родительский URL-адрес конечного не существует. Нет опечатки в URL-адрес источника или назначения. Может быть https://mysite/photo/myphoto.jpg при фактически должен иметь https://mysite/photos/myphoto.jpg вместо этого. Ошибка ввода в URL-адрес родительского (в данном случае <em>фотографий</em> вместо <em>фотографии</em>) вызвала ошибку.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>Недостаточно разрешений для доступа к дерево или поддерево. Пользователя, указанного в строке подключения не имеет соответствующие разрешения.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>URL-адрес содержит недопустимые символы. Убедитесь в том, что URL-адрес введен правильно. URL-адрес, исходя из схемы, зарегистрированных для текущего поставщика (например, Internet публикации регистрируется поставщик для http).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>Объект, представленный указанным URL-адрес заблокирован один или несколько других процессов. Дождитесь завершения процесса и повторите попытку выполнения операции. Объект, который вы пытаетесь получить доступ был заблокирован другим пользователем или другим процессом в приложении. Это наиболее могут возникнуть в многопользовательской среде.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>Невозможно выполнить операцию копирования. Объект с именем, URL-адрес назначения уже существует. Укажите <strong>adCopyOverwrite</strong> объект. Если <strong>adCopyOverwrite</strong> не указан, при копировании файлов в каталоге, копии происходит сбой при попытке скопировать элемент, который уже существует в месте назначения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>Сервер не может завершить операцию. Возможно, сервер занят с других операций или не хватает ресурсов.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>Поставщик может найти запоминающее устройство, указанный в параметре URL-адрес. Убедитесь в том, что URL-адрес введен правильно. URL-адрес устройства хранения может быть неправильная, но эта ошибка может возникнуть по другим причинам. Устройство может работать в автономном режиме или большой объем сетевого трафика может запретить подключение от использовались.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>Невозможно выполнить операцию. Поставщик не удается получить достаточно дискового пространства. Не возможно достаточного количества оперативной памяти или места на жестком диске для временных файлов на сервере.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>URL-адрес источника и назначения выходит за рамки текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>Не удалось завершить операцию и состояние недоступна. Поле может быть недоступна или не попытка выполнения операции. Может измененного или удаленного поле, которое вы пытаетесь получить доступ к другому пользователю.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>Запись с именем, этот URL-адрес не существует. При открытии файла с помощью объекта <strong>записи</strong> был неправильно имя файла и путь к файлу.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>URL-адрес объекта, к удалению выходит за рамки текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>Операции требуется допустимый <strong>ParentCatalog</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>Подключение было запрещено. Новое подключение запрошенный имеет разные характеристики, чем в уже используется.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Не удалось обновить поля. Для получения дополнительных сведений проверьте свойство <strong>Status</strong> объектов отдельного поля. Эта ошибка может возникнуть в двух случаях: при изменении значения объекта <strong>поля</strong> , изменение или Добавление записи в базу данных; и при изменении свойств сам объект <strong>поля</strong> . Не удалось обновить <strong>записи</strong> или <strong>записей</strong> из-за проблем с одного из полей в текущей записи. Перечисление коллекции <strong>полей</strong> и проверьте <strong>состояние</strong> свойство каждое поле, чтобы определить причину проблемы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает ограничения общего доступа. Предпринята попытка для ограничения доступа к файлам и ваш поставщик поддерживает концепцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает запрошенный тип общего доступа к ограничение. Предпринята попытка установить определенный тип доступа к файлам ограничение, которое не поддерживается поставщиком. В документации поставщика для определения поддерживаются ограничения доступа к файлам.</p></td>
</tr>
</tbody>
</table>

