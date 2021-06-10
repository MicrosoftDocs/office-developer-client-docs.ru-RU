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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283396"
---
# <a name="ado-error-reference"></a>Справочник по ошибкам ADO

**Область применения**: Access 2013, Office 2013

**Константа ErrorValueEnum** описывает значения ошибок ADO. Полный список указанных констант, включая значения, см. в приложении [B: ADO Errors.](appendix-b-ado-errors.md) В этом разделе рассматриваются некоторые из наиболее интересных ошибок и объясняются некоторые конкретные ситуации, которые могут привести к их повышению, или решения для устранения проблемы. Перечислены **как константа ErrorValueEnum,** так и короткий положительный десятичной номер.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Номер</p></th>
<th><p>Константа ErrorValueEnum</p></th>
<th><p>Описание/Возможные причины</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>Поставщик не выполнил запрашиваемую операцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Аргументы имеют неправильный тип, находятся вне допустимого диапазона или находятся в конфликте друг с другом. Эта ошибка часто вызвана опечаткой в SQL SELECT. Например, ошибочное имя поля или имя таблицы может создать эту ошибку. Эта ошибка также может возникать, когда поле или таблица, названная в заявлении SELECT, не существует в хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Файл не может быть открыт. Было задано имя файла с ошибками, или файл был перемещен, переименован или удален. В сети диск может быть временно недоступен, а сетевой трафик может препятствовать подключению.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Файл нельзя было прочитать. Имя файла указывается неправильно, файл мог быть перемещен или удален, или файл мог быть поврежден.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Написать файл не удалось. Возможно, вы закрыли файл, а затем попытались написать в него, или файл может быть поврежден. Если файл расположен на сетевом диске, временные условия сети могут помешать записи на сетевой диск.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>Либо <strong>BOF,</strong> <strong>либо EOF</strong> — true, либо текущая запись удалена. Запрашиваемая операция требует текущей записи. Была предпринята попытка обновить записи с помощью <strong>Find</strong> или <strong>Seek</strong> для перемещения указателя записи в нужную запись. Если запись не найдена, <strong>EOF</strong> будет true. Эта ошибка также может возникнуть после неудачного <strong>addNew</strong> или <strong>Delete,</strong> так как при сбойе этих методов нет текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>В этом контексте операция запрещена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>Поставщик, поставляемый, отличается от используемого поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции. Объект <strong>Recordset</strong> или <strong>Connection,</strong> который в настоящее время участвует в транзакции, не может быть закрыт. Перед закрытием объекта позвоните в <strong>RollbackTrans</strong> или <strong>CommitTrans.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>Объект или поставщик не способны выполнять запрашиваемую операцию. Некоторые операции зависят от конкретной версии поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>Элемент не может быть найден в коллекции, соответствующей запрашиваемой имени или ordinal. Задано неправильное поле или имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>Объект уже находится в коллекции. Не удается примять. Объект нельзя дважды добавлять в ту же коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>Объект больше не действителен.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>Приложение использует значение неправильного типа для текущей операции. Возможно, вы поставили строку для операции, которая ожидает поток, например.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>Операция не допускается при закрытии объекта. Подключение <strong>или</strong> <strong>набор записей</strong> закрыт. Например, некоторые другие процедуры могли закрыть глобальный объект. Эту ошибку можно предотвратить, проверив <strong>свойство state</strong> перед попыткой операции.</p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>Операция не допускается, когда объект открыт. Открытый объект не может быть открыт. Поля нельзя примыкать к открытому <strong>набору записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>Поставщик не может быть найден. Он может быть неправильно установлен. Имя поставщика может быть неправильно указано, указанный поставщик может не быть установлен на компьютере, на котором выполняется код, или установка может быть повреждена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>Свойство <strong>ActiveConnection</strong> объекта <strong>Recordset,</strong> который имеет объект <strong>Command</strong> в качестве источника, не может быть изменено. Приложение пыталось назначить новый объект <strong>Подключения</strong> к <strong>набору Recordset,</strong> который имеет <strong>объект Command</strong> в качестве источника.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p><strong>Объект параметра</strong> неправильно определен. Несогласованные или неполные сведения были предоставлены.</p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>Подключение не может использоваться для выполнения этой операции. В этом контексте она закрыта или недействительна.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>Операция не может выполняться во время обработки события. Операция не может выполняться в обработнике событий, из-за этого событие снова загорелось. Например, методы навигации не должны быть вызваны из обработника событий <strong>WillMove.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>Операция не может выполняться при асинхронном выполнении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>Операция была отменена пользователем. Приложение вызвало метод <strong>CancelUpdate</strong> или <strong>CancelBatch,</strong> и текущая операция была отменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>Операция не может выполняться при асинхронном подключении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>Координация транзакции недействительна или не запущена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>Операция не может выполняться при неоформлённой работе.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>Параметры безопасности на этом компьютере запрещают доступ к источнику данных на другом домене.</p></td>
</tr>
<tr class="even">
<td><p><strong>3717</strong></p></td>
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>Только для внутреннего использования. Не используйте. (Запись была включена для полноты. Эта ошибка не должна отображаться в коде.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>3718</strong></p></td>
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>Только для внутреннего использования. Не используйте. (Запись включена для полноты. Эта ошибка не должна отображаться в коде.)</p></td>
</tr>
<tr class="even">
<td><p><strong>3719</strong></p></td>
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>Значение data противоречит ограничениям целостности поля. Новое значение для <strong>поля приведет</strong> к дублирующему ключу. Значение, которое формирует одну сторону связи между двумя записями, может не быть updatable.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>Недостаточное разрешение препятствует записи в поле. Пользователь, названный в строке подключения, не имеет соответствующих разрешений для записи в <strong>поле</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>Значение данных слишком большое, чтобы представляться типом данных поля. Назначено численное значение, слишком большое для назначенного поля. Например, для короткого integer-поля было назначено длинное значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Значение данных противоречит типу данных или ограничениям поля. В хранилище данных имеются ограничения проверки, отличающиеся от <strong>значения Field.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>Преобразование не удалось, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не был подписан.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>Значение данных не может быть преобразовано по другим причинам, кроме несоответствия знака или переполнения данных. Например, преобразование будет иметь усеченные данные.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>Значение данных невозможно установить или получить, так как тип данных поля был неизвестным или у поставщика не было достаточных ресурсов для выполнения операции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>Запись не содержит этого поля. Было указано неправильное имя поля или поле, не указанное в коллекции <strong>Fields</strong> текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>Url-адрес источника или родитель URL-адреса не существует. В URL-адресе источника или назначения имеется опечатка. Возможно, у https://mysite/photo/myphoto.jpg вас будет время, когда вы должны иметь https://mysite/photos/myphoto.jpg вместо этого. Ошибка в родительском URL-адресе (в данном <em></em> случае фотография, а не <em>фотографии)</em>вызвала ошибку.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>Разрешений недостаточно для доступа к дереву или подтрию. Пользователь, названный в строке подключения, не имеет соответствующих разрешений.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>URL-адрес содержит недопустимые символы. Убедитесь, что URL-адрес введите правильно. URL-адрес следует схеме, зарегистрированной текущему поставщику (например, поставщик интернет-публикаций зарегистрирован для http).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами. Подождите, пока процесс завершится, и снова попытайтесь сделать операцию. Объект, к который вы пытаетесь получить доступ, был заблокирован другим пользователем или другим процессом в вашем приложении. Скорее всего, это может возникнуть в среде с несколькими пользователями.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>Операция копирования не может выполняться. Объект, названный URL-адресом назначения, уже существует. Укажите <strong>adCopyOverwrite для</strong> замены объекта. Если при копировании файлов в каталоге не указывается <strong>adCopyOverwrite,</strong> при попытке скопировать элемент, который уже существует в пункте назначения, копия не удается.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>Сервер не может завершить операцию. Возможно, это происходит из-за того, что сервер занят другими операциями или может иметь ограниченные ресурсы.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>Поставщик не может найти устройство хранения, обозначенное URL-адресом. Убедитесь, что URL-адрес введите правильно. URL-адрес устройства хранения может быть неправильным, но эта ошибка может возникнуть по другим причинам. Устройство может быть отключено, а большой объем сетевого трафика может помешать подключению.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>Операция не может быть выполнена. Поставщик не может получить достаточно места для хранения. На сервере может не быть достаточно места для оперативной памяти или жесткого диска для временных файлов.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>URL-адрес источника или назначения находится за пределами текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>Операция не завершена, и состояние недоступно. Поле может быть недоступно или операция не была предпринята. Другой пользователь мог изменить или удалить поле, к нему необходимо получить доступ.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>Запись, названная этим URL-адресом, не существует. При попытке открыть файл с помощью объекта <strong>Запись</strong> имя файла или путь к файлу был опечатка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>URL-адрес удаляемого объекта находится за пределами текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>Операция требует допустимого <strong>ParentCatalog</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>Подключение было отказано. Запрашиваемая вами новая связь отличается от используемого подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Обновление полей не удалось. Дополнительные сведения изучите свойство <strong>Status</strong> отдельных объектов поля. Эта ошибка может возникать в двух ситуациях: при изменении значения объекта <strong>Field</strong> в процессе изменения или добавления записи в базу данных; и при изменении свойств самого <strong>объекта Field.</strong> Обновление <strong>Record</strong> или <strong>Recordset</strong> не удалось из-за проблемы с одним из полей текущей записи. Перенапределяйте коллекцию <strong>Fields</strong> и проверьте свойство <strong>Status</strong> каждого поля, чтобы определить причину проблемы.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает ограничения общего доступа. Была предпринята попытка ограничить общий доступ к файлам, и поставщик не поддерживает эту концепцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает запрашиваемого вида ограничения общего доступа. Была предпринята попытка установить определенный тип ограничения общего доступа к файлам, который не поддерживается поставщиком. См. документацию поставщика, чтобы определить, какие ограничения для общего доступа к файлам поддерживаются.</p></td>
</tr>
</tbody>
</table>

