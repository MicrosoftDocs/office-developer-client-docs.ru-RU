---
title: Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 07031639b707fc24a3e5b057520c601c9472b01b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026318"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)

**Применимо к**: Access 2013, Office 2013

Поставщик удаленного взаимодействия Microsoft OLE DB позволяет локального пользователя на клиентском компьютере для вызова поставщиков данных на удаленном компьютере. Укажите параметры поставщика данных для удаленного компьютера, как если бы вы были локального пользователя на удаленном компьютере. Затем укажите параметры, используемый поставщиком удаленного взаимодействия для доступа к удаленному компьютеру. Итоговый результат — это будет доступ удаленного компьютера, как если бы вы были локального пользователя.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать поставщика OLE DB удаленного взаимодействия, укажите следующие ключевое слово и значение в строке подключения. (Примечание свободное место в имени поставщика и имени).

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Дополнительные ключевые слова

При вызове этого поставщика услуг относятся следующие дополнительные ключевые слова.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Keyword</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя к удаленному источнику данных. Он передается для поставщика OLE DB удаленного взаимодействия для обработки. Ключевое слово this эквивалентно <a href="datacontrol-object-rds.md">RDS. DataControl</a> <a href="connect-property-rds.md">Подключить</a> свойства объекта.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика услуг в семейство сайтов [Свойства](properties-collection-ado.md) объект [подключения](connection-object-ado.md) добавляются следующие динамические свойства.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя динамического свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Указывает режим DataFactory. Строка, определяющая рекомендуемой версии объекта <a href="datafactory-object-rdsserver.md">DataFactory</a> на сервере. Свойства перед открытием подключения к определенной версии <strong>DataFactory</strong>запроса. Если запрошенная версия недоступен, будет предпринята попытка использовать предыдущей версии. Если предыдущая версия не, произойдет ошибка. Если <strong>DFMode</strong> меньше, чем доступная версия, произойдет ошибка. Это свойство доступно только для чтения после установить соединение. Возможны следующие значения: допустимая строка:</p>
<p></p>
<ul>
<li><p>&quot;25&quot; — версии 2.5 (по умолчанию)</p></li>
<li><p>&quot;21&quot; — версии 2.1</p></li>
<li><p>&quot;20&quot; — версии 2.0</p></li>
<li><p>&quot;15&quot; — версия 1.5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Свойства команды</strong></p></td>
<td><p>Указывает значения, которые будут добавлены к строке свойства команды (строк), отправленные на сервер с поставщиком удаленного мс. Значение по умолчанию для этой строки — vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Текущий DFMode</strong></p></td>
<td><p>Указывает номер версии фактический <strong>DataFactory</strong> на сервере. Проверяет, это свойство, чтобы увидеть, если был учитываться версии, запрошенного в свойстве <strong>DFMode</strong> . Может иметь одно из следующих значений длинное целое число:</p>
<p></p>
<ul>
<li><p>25 — версии 2.5 (по умолчанию)</p></li>
<li><p>21 — версии 2.1</p></li>
<li><p>20 — версии 2.0</p></li>
<li><p>15 — версия 1.5</p></li>
</ul>
<p></p>
<p>Добавление &quot;DFMode = 20; &quot; для подключения к строку при использовании поставщика <strong>MSRemote</strong> можно улучшить производительность сервера при обновлении данных. С помощью этого параметра, режим менее интенсивно использует объект <strong>RDSServer.DataFactory</strong> на сервере. Тем не менее в этой конфигурации недоступны следующие функции:</p>
<p></p>
<ul>
<li><p>Использование запросов с параметрами.</p></li>
<li><p>Получение сведений о параметра или столбца до вызова метода <strong>Execute</strong> .</p></li>
<li><p>Установка <strong>обновлений Transact</strong> <strong>значения True</strong>.</p></li>
<li><p>Начало строки состояния.</p></li>
<li><p>Вызов метода <strong>выполнить повторную синхронизацию</strong> .</p></li>
<li><p>Обновление через свойство <strong>Выполнить повторную синхронизацию обновления</strong> (явно или автоматически).</p></li>
<li><p>Установка свойств <strong>команда</strong> или <strong>набора записей</strong> .</p></li>
<li><p>С помощью <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Обработчик</strong></p></td>
<td><p>Указывает имя программы настройки на сервере (или обработчик), который расширяет возможности <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>и все параметры, используемые обработчиком<em>,</em> все, разделив их запятыми (&quot;,&quot;). <strong>Строковое</strong> значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Время ожидания для Интернета</strong></p></td>
<td><p>Указывает максимальное количество миллисекундах время ожидания для передачи запроса на сервер и с него. (Значение по умолчанию — 5 минут).</p></td>
</tr>
<tr class="even">
<td><p><strong>Удаленный поставщик</strong></p></td>
<td><p>Указывает имя поставщика данных для использования на удаленном сервере.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Удаленный сервер</strong></p></td>
<td><p>Указывает имя и связи протоколом использованный для данного подключения. Это свойство соответствует параметру <a href="datacontrol-object-rds.md">RDS. DataControl</a> объекта свойства <a href="server-property-rds.md">сервера</a> .</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact обновлений</strong></p></td>
<td><p>Если задано значение True, это значение указывает, что при <a href="updatebatch-method-ado.md">UpdateBatch</a> выполняется на сервере, это будет выполнено, внутри транзакции. Значение по умолчанию для этого типа Boolean динамические свойства имеет значение False.</p></td>
</tr>
</tbody>
</table>


Можно также установить для записи динамические свойства путем указания их имена в качестве ключевых слов в строке подключения. К примеру присвойте свойству динамических **Время ожидания для Интернета** на пять секунд путем указания:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Можно также задать или получить динамического свойства, указав его имя в качестве индекса в **поле свойства** . К примеру получить и печать текущее значение свойства динамических **Время ожидания для Интернета** и задайте новое значение, следующим образом.

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Примечания

В ADO 2.0 поставщик OLE DB об удаленном взаимодействии может быть указан только с помощью параметра *ActiveConnection* метод **Open** объекта [набора записей](recordset-object-ado.md) . Начиная с ADO 2.1, поставщик может также быть указано в параметре *ConnectionString* объекта [подключения к](connection-object-ado.md) методу **Open** .

Эквивалент **RDS. DataControl** объект свойство [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) не поддерживается. Вместо этого используется метод **Open** *исходный* аргумент объекта [набора записей](recordset-object-ado.md) .

Указание «...; Удаленный поставщик = удаленного мс;...» Создать сценарий четыре уровня. Сценарии, чем три уровня не проверялись и не должно быть необходимым.

## <a name="example"></a>Пример

В этом примере выполняется запрос на таблице **авторов** **pubs** базы данных на сервере с именем, *сервер*. Имена удаленному источнику данных и удаленный сервер предоставляются в метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) и SQL-запрос, указанный в метод [Open](open-method-ado-recordset.md) объекта [набора записей](recordset-object-ado.md) . Объект **набора записей** возвращается, редактировать и используется для обновления источника данных.

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

