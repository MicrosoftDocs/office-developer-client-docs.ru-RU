---
title: Коды ошибок DataControl
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 387f37e180d346c09cf3dadbf66f665cb83dbd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294546"
---
# <a name="datacontrol-error-codes"></a>Коды ошибок DataControl


**Область применения**: Access 2013, Office 2013

В следующей таблице [перечислены RDS. Коды ошибок объектов DataControl.](datacontrol-object-rds.md) Показан положительный десятичной перевод низких двух bytes, отрицательный десятичной перевод полного кода ошибки и гексадецимальные значения.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>RDS. Коды ошибок DataControl</p></th>
<th><p>Номер</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>IDS_AsyncPending</strong></p></td>
<td><p>4107<br />
-2146824175<br />
0x800A1011</p></td>
<td><p>Операция не может выполняться во время ожидания операции async.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_BadInlineTablegram</strong></p></td>
<td><p>4105<br />
-2146824183<br />
0x800A1009</p></td>
<td><p>Плохая inline tablegram.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantConnect</strong></p></td>
<td><p>4099<br />
-2146824189<br />
0x800A1003</p></td>
<td><p>Невозможно подключиться к серверу.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantCreateObject</strong></p></td>
<td><p>4100<br />
-2146824188<br />
0x800A1004</p></td>
<td><p>Бизнес-объект не может быть создан.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CantFindDataspace</strong></p></td>
<td><p>4102<br />
-2146824186<br />
0x800A1006</p></td>
<td><p>Свойство Dataspace не является допустимым.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_CantInvokeMethod</strong></p></td>
<td><p>4101<br />
-2146824187<br />
0x800A1005</p></td>
<td><p>Метод не может вызываться в бизнес-объекте.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_CrossDomainWarning</strong></p></td>
<td><p>4112<br />
-2146824170<br />
0x800A1016</p></td>
<td><p>Эта страница имеет доступ к данным на другом домене. Вы хотите разрешить это? Чтобы избежать этого сообщения в Internet Explorer, можно добавить безопасный <strong></strong> веб-сайт в зону доверенных сайтов на вкладке Безопасность диалогового окна <strong>"Параметры</strong> Интернета".</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidADCClientVersion</strong></p></td>
<td><p>4106<br />
-2146824176<br />
0x800A1010</p></td>
<td><p>Недействительный клиентская версия RDS — клиент является более новым, чем сервер.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_INVALIDARG</strong></p></td>
<td><p>5376<br />
-2147019520<br />
0x80071500</p></td>
<td><p>Один или несколько аргументов являются недействительными.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_InvalidBindings</strong></p></td>
<td><p>4097<br />
-2146824191<br />
0x800A1001</p></td>
<td><p>Ошибка в свойстве привязки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_InvalidParam</strong></p></td>
<td><p>4110<br />
-2146824172<br />
0x800A1014</p></td>
<td><p>Один или несколько аргументов являются недействительными.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_NOINTERFACE</strong></p></td>
<td><p>5377<br />
-2147019519<br />
0x80071501</p></td>
<td><p>Такой интерфейс не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_NotReentrant</strong></p></td>
<td><p>4111<br />
-2146824171<br />
0x800A1015</p></td>
<td><p>Запрос нельзя выполнять, пока обработник событий еще обрабатывается.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ObjectNotSafe</strong></p></td>
<td><p>4103<br />
-2146824185<br />
0x800A1007</p></td>
<td><p>Параметры безопасности на этом компьютере запрещают создание бизнес-объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RecordsetNotOpen</strong></p></td>
<td><p>4109<br />
-2146824173<br />
0x800A1013</p></td>
<td><p><strong>Набор записей</strong> не открыт.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_ResetInvalidField</strong></p></td>
<td><p>4108<br />
-2146824174<br />
0x800A1012</p></td>
<td><p>Столбец, <strong>указанный в SortColumn или</strong> <strong>FilterColumn,</strong> не существует.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_RowsetNotUpdateable</strong></p></td>
<td><p>4104<br />
-2146824184<br />
0x800A1008</p></td>
<td><p>Rowset не обновляется.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_UnexpectedError</strong></p></td>
<td><p>4351<br />
-2146823937<br />
0x800A10FF</p></td>
<td><p>Неожиданная ошибка.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IDS_UpdatesFailed</strong></p></td>
<td><p>4098<br />
-2146824190<br />
0x800A1002</p></td>
<td><p>Невозможно обновить базу данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>IDS_URLMONNotFound</strong></p></td>
<td><p>4119<br />
-2146824169<br />
0x800A1017</p></td>
<td><p>Свойство URL-адреса <strong>DataControl</strong> требует Urlmon.dll файла системы, который невозможно найти.</p></td>
</tr>
</tbody>
</table>

