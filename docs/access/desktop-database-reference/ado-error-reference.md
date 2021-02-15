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

**Константа ErrorValueEnum** описывает значения ошибок ADO. Полный список этих перечисляемых констант, включая значения, см. в приложении [Б. Ошибки ADO.](appendix-b-ado-errors.md) В этом разделе рассматриваются некоторые наиболее интересные ошибки и поясняются некоторые конкретные ситуации, которые могут их привести, или решения для устранения проблемы. В **списке указаны как константа ErrorValueEnum,** так и короткое положительное десятичность.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Числовой</p></th>
<th><p>Константа ErrorValueEnum</p></th>
<th><p>Описание/Возможные причины</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>3000</strong></p></td>
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>Поставщику не удалось выполнить запрашиваемую операцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>3001</strong></p></td>
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом. Эта ошибка часто вызвана опечаткой в SQL SELECT. Например, эта ошибка может быть опечатка имени поля или таблицы. Эта ошибка также может возникать, если поле или таблица, именуемая в заявлении SELECT, не существует в хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3002</strong></p></td>
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>Не удалось открыть файл. Было указано имя файла с ошибками или файл был перемещен, переименован или удален. По сети диск может быть временно недоступен или сетевой трафик может препятствовать подключению.</p></td>
</tr>
<tr class="even">
<td><p><strong>3003</strong></p></td>
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>Не удалось прочитать файл. Имя файла указано неправильно, возможно, файл был перемещен или удален либо файл поврежден.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3004</strong></p></td>
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>Сбой записи в файл. Возможно, вы закрыли файл, а затем попытались записать его, или файл может быть поврежден. Если файл находится на сетевом диске, временные сетевые условия могут препятствовать записи на сетевой диск.</p></td>
</tr>
<tr class="even">
<td><p><strong>3021</strong></p></td>
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>Либо <strong>BOF,</strong> <strong>либо EOF</strong> имеет true, либо текущая запись была удалена. Для запрашиваемой операции требуется текущая запись. Была предпринята попытка обновить записи <strong></strong> с помощью поиска или поиска, чтобы переместить указатель записи в нужную запись. <strong></strong> Если запись не найдена, <strong>EOF</strong> будет иметь true. Эта ошибка также может возникать после с ошибки <strong>AddNew</strong> или <strong>Delete,</strong> так как при с ошибке этих методов нет текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3219</strong></p></td>
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>В этом контексте операция не разрешена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3220</strong></p></td>
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>Поставщик отличается от поставщика, который уже используется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3246</strong></p></td>
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции. Объект <strong>Recordset</strong> или <strong>Connection,</strong> который в настоящее время участвует в транзакции, не может быть закрыт. Вызовите <strong>RollbackTrans или</strong> <strong>CommitTrans</strong> перед закрытием объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>3251</strong></p></td>
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>Объект или поставщик не могут выполнить запрашиваемую операцию. Некоторые операции зависят от конкретной версии поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3265</strong></p></td>
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>Не удается найти элемент в коллекции, соответствующей запросятово имени или порядку. Указано неправильное поле или имя таблицы.</p></td>
</tr>
<tr class="even">
<td><p><strong>3367</strong></p></td>
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>Объект уже находится в коллекции. Не удается приметься. Объект нельзя добавить в ту же коллекцию дважды.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3420</strong></p></td>
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>Объект больше не действителен.</p></td>
</tr>
<tr class="even">
<td><p><strong>3421</strong></p></td>
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>Приложение использует неправильное значение для текущей операции. Возможно, вы предоставили строку для операции, которая ожидает потока, например.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3704</strong></p></td>
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>Операция не разрешена при закрытии объекта. Подключение <strong>или</strong> <strong>набор записей</strong> закрыты. Например, другая процедура могла закрыть глобальный объект. Эту ошибку можно предотвратить, проверив свойство <strong>State</strong> перед попыткой операции.</p></td>
</tr>
<tr class="even">
<td><p><strong>3705</strong></p></td>
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>Операция не разрешена, если объект открыт. Открытый объект не может быть открыт. Поля нельзя примедить к открытому <strong>набору записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>3706</strong></p></td>
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>Не удается найти поставщика. Он может быть неправильно установлен. Имя поставщика может быть указано неправильно, указанный поставщик может не быть установлен на компьютере, на котором выполняется код, или установка может быть повреждена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3707</strong></p></td>
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>Свойство <strong>ActiveConnection</strong> объекта <strong>Recordset,</strong> в качестве источника которого имеется объект <strong>Command,</strong> нельзя изменить. Приложение попытались назначить новый объект <strong>Connection</strong> <strong>объекту Recordset,</strong> который имеет объект <strong>Command</strong> в качестве источника.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3708</strong></p></td>
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p><strong>Объект Parameter</strong> определен неправильно. Предоставлены несогласованные или неполные сведения.</p></td>
</tr>
<tr class="even">
<td><p><strong>3709</strong></p></td>
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>Подключение нельзя использовать для выполнения этой операции. В этом контексте он либо закрыт, либо недействителен.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3710</strong></p></td>
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>Операция не может быть выполнена во время обработки события. Невозможно выполнить операцию в обработнике событий, который вызывает повторную работу события. Например, методы навигации не должны быть вызваны из <strong>обработника событий WillMove.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3711</strong></p></td>
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>Операция не может выполняться при асинхронном выполнении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3712</strong></p></td>
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>Операция была отменена пользователем. Приложение вызвало метод <strong>CancelUpdate</strong> или <strong>CancelBatch,</strong> а текущая операция была отменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3713</strong></p></td>
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>Операция не может выполняться при асинхронном подключении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3714</strong></p></td>
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>Транзакция координации недействительна или не запущена.</p></td>
</tr>
<tr class="even">
<td><p><strong>3715</strong></p></td>
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>Не удается выполнить операцию, пока она не выполняется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3716</strong></p></td>
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>Параметры безопасности на этом компьютере запрещают доступ к источнику данных в другом домене.</p></td>
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
<td><p>Значение данных конфликтет с ограничениями целостности поля. Новое значение поля <strong>приведет</strong> к дублированию ключа. Значение, которое формирует одну сторону связи между двумя записями, может быть не может быть updatable.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3720</strong></p></td>
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>Недостаточное разрешение препятствует записи в поле. У пользователя, имя которого есть в строке подключения, нет необходимых разрешений для записи в <strong>поле.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3721</strong></p></td>
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>Значение данных слишком большое для представления типом данных поля. Назначено числовая величина, слишком большая для назначенного поля. Например, длинное значение было назначено короткому полю.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3722</strong></p></td>
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>Значение данных конфликтет с типом данных или ограничениями поля. Хранилище данных имеет ограничения проверки, отличающиеся от <strong>значения Field.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>3723</strong></p></td>
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>Сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3724</strong></p></td>
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>Значение данных не может быть преобразовано по другим причинам, кроме несоответствия подписей или переполнения данных. Например, преобразование будет иметь усеченные данные.</p></td>
</tr>
<tr class="even">
<td><p><strong>3725</strong></p></td>
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>Значение данных нельзя установить или извлечь, так как тип данных поля был неизвестным, или у поставщика недостаточно ресурсов для выполнения операции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3726</strong></p></td>
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>Запись не содержит это поле. Было указано неправильное имя поля или поле, не в которое в коллекции <strong>Fields</strong> текущей записи была указана ссылка.</p></td>
</tr>
<tr class="even">
<td><p><strong>3727</strong></p></td>
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>Исходный URL-адрес или родительский URL-адрес назначения не существуют. В URL-адресе источника или назначения имеется опечатка. Возможно, у https://mysite/photo/myphoto.jpg вас будет время, когда вы действительно должны https://mysite/photos/myphoto.jpg иметь вместо этого. Опечатка в родительском URL-адресе (в данном случае <em>фотография,</em> а не <em>фотографии)</em>вызвала ошибку.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3728</strong></p></td>
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>Недостаточно разрешений для доступа к дереву или подtree. Пользователь с именем в строке подключения не имеет соответствующих разрешений.</p></td>
</tr>
<tr class="even">
<td><p><strong>3729</strong></p></td>
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>URL-адрес содержит недопустимые символы. Убедитесь, что URL-адрес введите правильно. URL-адрес следует схеме, зарегистрированной для текущего поставщика (например, поставщик публикации Интернета зарегистрирован для http).</p></td>
</tr>
<tr class="odd">
<td><p><strong>3730</strong></p></td>
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами. Подождите, пока процесс завершится, и снова попытайтесь повторить операцию. Объект, к который вы пытаетесь получить доступ, заблокирован другим пользователем или другим процессом в приложении. Скорее всего, это может возникнуть в среде с несколькими пользователями.</p></td>
</tr>
<tr class="even">
<td><p><strong>3731</strong></p></td>
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>Не удается выполнить операцию копирования. Объект с именем по url-адресу назначения уже существует. Укажите <strong>adCopyOverwrite для</strong> замены объекта. Если при копировании файлов в каталоге не указан <strong>adCopyOverwrite,</strong> то при попытке скопировать элемент, который уже существует в месте назначения, происходит сбой копирования.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3732</strong></p></td>
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>Сервер не может завершить операцию. Это может быть из-за того, что сервер занят другими операциями или у него может быть мало ресурсов.</p></td>
</tr>
<tr class="even">
<td><p><strong>3733</strong></p></td>
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>Поставщик не может найти устройство хранения, обозначенное URL-адресом. Убедитесь, что URL-адрес введите правильно. URL-адрес устройства хранения может быть неправильным, но эта ошибка может возникнуть по другим причинам. Устройство может быть отключено или большой объем сетевого трафика может препятствовать подключению.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3734</strong></p></td>
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>Не удается выполнить операцию. Поставщик не может получить достаточно места для хранения. На сервере может быть недостаточно места на ОЗУ или жестком диске для временных файлов.</p></td>
</tr>
<tr class="even">
<td><p><strong>3735</strong></p></td>
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>Url-адрес источника или назначения находится за пределами области текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3736</strong></p></td>
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>Не удалось завершить операцию, и состояние недоступно. Поле может быть недоступно или операция не была предпринята. Другой пользователь мог изменить или удалить поле, к нему вы пытаетесь получить доступ.</p></td>
</tr>
<tr class="even">
<td><p><strong>3737</strong></p></td>
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>Запись с именем по этому URL-адресу не существует. При попытке открыть файл с помощью объекта <strong>Record</strong> имя файла или путь к файлу был опечаток.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3738</strong></p></td>
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>URL-адрес удаляемого объекта находится вне области текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>3747</strong></p></td>
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>Для операции требуется <strong>допустимый parentCatalog.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>3748</strong></p></td>
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>Подключение было отклонено. Запрашиваемая вами новая связь имеет характеристики, отлича которые уже используются.</p></td>
</tr>
<tr class="even">
<td><p><strong>3749</strong></p></td>
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>Сбой обновления полей. Для получения дополнительных сведений <strong>изучите свойство Status</strong> отдельных объектов полей. Эта ошибка может возникать в двух ситуациях: при изменении значения объекта <strong>Field</strong> в процессе изменения или добавления записи в базу данных; и при изменении свойств самого <strong>объекта Field.</strong> <strong>Сбой</strong> обновления record или <strong>Recordset</strong> из-за проблемы с одним из полей в текущей записи. Enumerate the <strong>Fields</strong> collection and check the <strong>Status</strong> property of each field to determine the cause of the problem.</p></td>
</tr>
<tr class="odd">
<td><p><strong>3750</strong></p></td>
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает ограничения общего доступа. Предпринята попытка ограничить общий доступ к файлам, и поставщик не поддерживает эту концепцию.</p></td>
</tr>
<tr class="even">
<td><p><strong>3751</strong></p></td>
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>Поставщик не поддерживает запрашиваемого типа ограничения общего доступа. Предпринята попытка установить определенный тип ограничения общего доступа к файлам, который не поддерживается поставщиком. Чтобы определить, какие ограничения общего доступа к файлам поддерживаются, см. документацию поставщика.</p></td>
</tr>
</tbody>
</table>

