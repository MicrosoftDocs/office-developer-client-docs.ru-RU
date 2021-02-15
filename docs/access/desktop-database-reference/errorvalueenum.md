---
title: ErrorValueEnum (справочник по базам данных Access для настольных ПК)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293324"
---
# <a name="errorvalueenum"></a>ErrorValueEnum

**Область применения**: Access 2013, Office 2013

Указывает тип ошибки во время работы ADO.

Перечислены три формы номера ошибки:

- Положительное десятичной затравка — низкий двухбайт полного числа в десятичной форме. Этот номер отображается в диалоговом окне Visual Basic сообщения об ошибке по умолчанию. Например, ошибка времени запуска "3707".

- Отрицательный десятичной зачет — десятичной перевод полного номера ошибки.

- Hexadecimal — hexadecimal representation of the full error number. Код объекта Windows находится в четвертой цифре. The facility code for ADO error numbers is *A*. Например: 0x800 ***A*** 0E7B.

> [!NOTE]
> Ошибки OLE DB могут передаваться в приложение ADO. Как правило, их можно определить с помощью кода объекта Windows *4.* Например, 0x800_ **4** _.... Дополнительные сведения об этих номерах см. в главе 16 справочника программиста *OLE DB.*

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adErrBoundToCommand</strong></p></td>
<td><p>3707<br />
-2146824581<br />
0x800A0E7B</p></td>
<td><p>Не удается изменить <strong>свойство ActiveConnection</strong> объекта <strong>Recordset,</strong> в качестве источника которого имеется объект <strong>Command.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCannotComplete</strong></p></td>
<td><p>3732<br />
-2146824556<br />
0x800A0E94</p></td>
<td><p>Сервер не может завершить операцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantChangeConnection</strong></p></td>
<td><p>3748<br />
-2146824540<br />
0x800A0EA4</p></td>
<td><p>Подключение было отклонено. Характеристики нового подключения отличаются от уже используемого.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantChangeProvider</strong></p></td>
<td><p>3220<br />
-2146825068<br />
0X800A0C94</p></td>
<td><p>Поставщик отличается от поставщика, который уже используется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCantConvertvalue</strong></p></td>
<td><p>3724<br />
-2146824564<br />
0x800A0E8C</p></td>
<td><p>Значение данных не может быть преобразовано по другим причинам, кроме несоответствия подписей или переполнения данных. Например, преобразование будет иметь усеченные данные.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrCantCreate</strong></p></td>
<td><p>3725<br />
-2146824563<br />
0x800A0E8D</p></td>
<td><p>Значение данных нельзя установить или извлечь, так как тип данных поля был неизвестным, или у поставщика недостаточно ресурсов для выполнения операции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrCatalogNotSet</strong></p></td>
<td><p>3747<br />
-2146824541<br />
0x800A0EA3</p></td>
<td><p>Для операции требуется <strong>допустимый parentCatalog.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adErrColumnNotOnThisRow</strong></p></td>
<td><p>3726<br />
-2146824562<br />
0x800A0E8E</p></td>
<td><p>Запись не содержит это поле.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDataConversion</strong></p></td>
<td><p>3421<br />
-2146824867<br />
0x800A0D5D</p></td>
<td><p>Приложение использует неправильное значение для текущей операции.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDataOverflow</strong></p></td>
<td><p>3721<br />
-2146824567<br />
0x800A0E89</p></td>
<td><p>Значение данных слишком большое для представления типом данных поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDelResOutOfScope</strong></p></td>
<td><p>3738<br />
-2146824550<br />
0x800A0E9A</p></td>
<td><p>URL-адрес удаляемого объекта находится вне области текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrDenyNotSupported</strong></p></td>
<td><p>3750<br />
-2146824538<br />
0x800A0EA6</p></td>
<td><p>Поставщик не поддерживает ограничения общего доступа.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrDenyTypeNotSupported</strong></p></td>
<td><p>3751<br />
-2146824537<br />
0x800A0EA7</p></td>
<td><p>Поставщик не поддерживает запрашиваемого типа ограничения общего доступа.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrFeatureNotAvailable</strong></p></td>
<td><p>3251<br />
-2146825037<br />
0x800A0CB3</p></td>
<td><p>Объект или поставщик не могут выполнять запрашиваемую операцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrFieldsUpdateFailed</strong></p></td>
<td><p>3749<br />
-2146824539<br />
0x800A0EA5</p></td>
<td><p>Сбой обновления полей. Для получения дополнительных сведений <strong>изучите свойство Status</strong> отдельных объектов полей.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrIllegalOperation</strong></p></td>
<td><p>3219<br />
-2146825069<br />
0x800A0C93</p></td>
<td><p>В этом контексте операция не разрешена.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrIntegrityViolation</strong></p></td>
<td><p>3719<br />
-2146824569<br />
0x800A0E87</p></td>
<td><p>Значение данных конфликтет с ограничениями целостности поля.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInTransaction</strong></p></td>
<td><p>3246<br />
-2146825042<br />
0x800A0CAE</p></td>
<td><p><strong>Объект подключения</strong> не может быть явно закрыт во время транзакции.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidArgument</strong></p></td>
<td><p>3001<br />
-2146825287<br />
0x800A0BB9</p></td>
<td><p>Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidConnection</strong></p></td>
<td><p>3709<br />
-2146824579<br />
0x800A0E7D</p></td>
<td><p>Подключение нельзя использовать для выполнения этой операции. В этом контексте он либо закрыт, либо недействителен.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidParamInfo</strong></p></td>
<td><p>3708<br />
-2146824580<br />
0x800A0E7C</p></td>
<td><p><strong>Объект Parameter</strong> определен неправильно. Предоставлены несогласованные или неполные сведения.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrInvalidTransaction</strong></p></td>
<td><p>3714<br />
-2146824574<br />
0x800A0E82</p></td>
<td><p>Координация транзакции недействительна или не запущена.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrInvalidURL</strong></p></td>
<td><p>3729<br />
-2146824559<br />
0x800A0E91</p></td>
<td><p>URL-адрес содержит недопустимые символы. Убедитесь, что URL-адрес введите правильно.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrItemNotFound</strong></p></td>
<td><p>3265<br />
-2146825023<br />
0x800A0CC1</p></td>
<td><p>Элемент не может быть найден в коллекции, соответствующей запрашиваемой именем или порядку.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNoCurrentRecord</strong></p></td>
<td><p>3021<br />
-2146825267<br />
0x800A0BCD</p></td>
<td><p>Либо <strong>BOF,</strong> <strong>либо EOF</strong> имеет true, либо текущая запись была удалена. Для запрашиваемой операции требуется текущая запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrNotExecuting</strong></p></td>
<td><p>3715<br />
-2146824573<br />
0x800A0E83</p></td>
<td><p>Не удается выполнить операцию, пока она не выполняется.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrNotReentrant</strong></p></td>
<td><p>3710<br />
-2146824578<br />
0x800A0E7E</p></td>
<td><p>Операция не может быть выполнена во время обработки события.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectClosed</strong></p></td>
<td><p>3704<br />
-2146824584<br />
0x800A0E78</p></td>
<td><p>Операция не разрешена при закрытии объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectInCollection</strong></p></td>
<td><p>3367<br />
-2146824921<br />
0x800A0D27</p></td>
<td><p>Объект уже находится в коллекции. Не удается приметься.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrObjectNotSet</strong></p></td>
<td><p>3420<br />
-2146824868<br />
0x800A0D5C</p></td>
<td><p>Объект больше не действителен.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrObjectOpen</strong></p></td>
<td><p>3705<br />
-2146824583<br />
0x800A0E79</p></td>
<td><p>Операция не разрешена, если объект открыт.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOpeningFile</strong></p></td>
<td><p>3002<br />
-2146825286<br />
0x800A0BBA</p></td>
<td><p>Не удалось открыть файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrOperationCancelled</strong></p></td>
<td><p>3712<br />
-2146824576<br />
0x800A0E80</p></td>
<td><p>Операция была отменена пользователем.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrOutOfSpace</strong></p></td>
<td><p>3734<br />
-2146824554<br />
0x800A0E96</p></td>
<td><p>Не удается выполнить операцию. Поставщик не может получить достаточно места для хранения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrPermissionDenied</strong></p></td>
<td><p>3720<br />
-2146824568<br />
0x800A0E88</p></td>
<td><p>Ненамеренное разрешение предотвращает запись в поле.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrProviderFailed</strong></p></td>
<td><p>3000<br />
-2146825288<br />
0x800A0BB8</p></td>
<td><p>Поставщику не удалось выполнить запрашиваемую операцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrProviderNotFound</strong></p></td>
<td><p>3706<br />
-2146824582<br />
0x800A0E7A</p></td>
<td><p>Не удается найти поставщика. Он может быть неправильно установлен.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrReadFile</strong></p></td>
<td><p>3003<br />
-2146825285<br />
0x800A0BBB</p></td>
<td><p>Не удалось прочитать файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceExists</strong></p></td>
<td><p>3731<br />
-2146824557<br />
0x800A0E93</p></td>
<td><p>Не удается выполнить операцию копирования. Объект с именем по url-адресу назначения уже существует. Укажите <strong>adCopyOverwrite для</strong> замены объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrResourceLocked</strong></p></td>
<td><p>3730<br />
-2146824558<br />
0x800A0E92</p></td>
<td><p>Объект, представленный указанным URL-адресом, блокируется одним или более другими процессами. Подождите, пока процесс завершится, и снова попытайтесь повторить операцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrResourceOutOfScope</strong></p></td>
<td><p>3735<br />
-2146824553<br />
0x800A0E97</p></td>
<td><p>Url-адрес источника или назначения находится вне области текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrSchemaViolation</strong></p></td>
<td><p>3722<br />
-2146824566<br />
0x800A0E8A</p></td>
<td><p>Значение данных конфликтет с типом данных или ограничениями поля.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrSignMismatch</strong></p></td>
<td><p>3723<br />
-2146824565<br />
0x800A0E8B</p></td>
<td><p>Сбой преобразования, так как значение данных было подписано, а тип данных поля, используемый поставщиком, не подписан.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrStillConnecting</strong></p></td>
<td><p>3713<br />
-2146824575<br />
0x800A0E81</p></td>
<td><p>Операция не может выполняться при асинхронном подключении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrStillExecuting</strong></p></td>
<td><p>3711<br />
-2146824577<br />
0x800A0E7F</p></td>
<td><p>Операция не может выполняться при асинхронном выполнении.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrTreePermissionDenied</strong></p></td>
<td><p>3728<br />
-2146824560<br />
0x800A0E90</p></td>
<td><p>Недостаточно разрешений для доступа к дереву или подtree.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrUnavailable</strong></p></td>
<td><p>3736<br />
-2146824552<br />
0x800A0E98</p></td>
<td><p>Не удалось завершить операцию, и состояние недоступно. Поле может быть недоступно или операция не была предпринята.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrUnsafeOperation</strong></p></td>
<td><p>3716<br />
-2146824572<br />
0x800A0E84</p></td>
<td><p>Параметры безопасности на этом компьютере запрещают доступ к источнику данных в другом домене.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrURLDoesNotExist</strong></p></td>
<td><p>3727<br />
-2146824561<br />
0x800A0E8F</p></td>
<td><p>Исходный URL-адрес или родительский URL-адрес назначения не существуют.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrURLNamedRowDoesNotExist</strong></p></td>
<td><p>3737<br />
-2146824551<br />
0x800A0E99</p></td>
<td><p>Запись с именем по этому URL-адресу не существует.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adErrVolumeNotFound</strong></p></td>
<td><p>3733<br />
-2146824555<br />
0x800A0E95</p></td>
<td><p>Поставщик не может найти устройство хранения, обозначенное URL-адресом. Убедитесь, что URL-адрес введите правильно.</p></td>
</tr>
<tr class="even">
<td><p><strong>adErrWriteFile</strong></p></td>
<td><p>3004<br />
-2146825284<br />
0x800A0BBC</p></td>
<td><p>Сбой записи в файл.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adWrnSecurityDialog</strong></p></td>
<td><p>3717<br />
-2146824571<br />
0x800A0E85</p></td>
<td><p>Только для внутреннего использования. Не используйте.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWrnSecurityDialogHeader</strong></p></td>
<td><p>3718<br />
-2146824570<br />
0x800A0E86</p></td>
<td><p>Только для внутреннего использования. Не используйте.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

Определены только следующие подмесяки эквивалентов ADO/WFC.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.BOUNDTOCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.DATACONVERSION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.FEATURENOTAVAILABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.ILLEGALOPERATION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INTRANSACTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDARGUMENT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.INVALIDCONNECTION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.INVALIDPARAMINFO</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.ITEMNOTFOUND</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOCURRENTRECORD</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.NOTEXECUTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.NOTREENTRANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTCLOSED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTINCOLLECTION</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OBJECTNOTSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.OBJECTOPEN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.OPERATIONCANCELLED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.PROVIDERNOTFOUND</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.STILLCONNECTING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ErrorValue.STILLEXECUTING</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ErrorValue.UNSAFEOPERATION</p></td>
</tr>
</tbody>
</table>

