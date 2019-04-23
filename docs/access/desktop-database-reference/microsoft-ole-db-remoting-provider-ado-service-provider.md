---
title: Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54ea659aa5392dd4404ffb591eba06f1f9c2910b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288906"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)

**Область применения**: Access 2013, Office 2013

Поставщик удаленного взаимодействия Microsoft OLE DB позволяет локальному пользователю на клиентском компьютере запускать поставщики данных на удаленном компьютере. Укажите параметры поставщика данных для удаленного компьютера так же, как если бы вы были локальными пользователями на удаленном компьютере. Затем укажите параметры, используемые поставщиком удаленного взаимодействия для доступа к удаленному компьютеру. Полученный результат заключается в том, что вы получите доступ к удаленному компьютеру, как если бы вы были локальным пользователем.

## <a name="provider-keyword"></a>Ключевое слово Provider

Чтобы вызвать поставщик удаленного взаимодействия OLE DB, укажите следующее ключевое слово и значение в строке подключения. (Обратите внимание на пустое пространство в имени поставщика.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Дополнительные ключевые слова

При вызове этого поставщика услуг важны следующие дополнительные ключевые слова.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Задает имя удаленного источника данных. Он передается поставщику удаленного взаимодействия OLE DB для обработки. Это ключевое слово эквивалентно <a href="datacontrol-object-rds.md">RDS. </a>Свойство <a href="connect-property-rds.md">Connect</a> объекта DataObject.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика услуг следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта [Connection](connection-object-ado.md) .

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
<td><p><strong>Дфмоде</strong></p></td>
<td><p>Указывает режим фактического режима. Строка, указывающая желаемую версию объекта <a href="datafactory-object-rdsserver.md">фактического</a> объекта на сервере. Задайте это свойство перед открытием подключения, чтобы запросить определенную версию объекта <strong>фактов</strong>. Если запрошенная версия недоступна, будет предпринята попытка использовать предыдущую версию. Если предыдущая версия отсутствует, возникнет ошибка. Если <strong>дфмоде</strong> меньше, чем доступная версия, возникнет ошибка. Это свойство доступно только для чтения после того, как подключение установлено. Может быть одним из следующих допустимых строковых значений:</p>
<p></p>
<ul>
<li><p>&quot;25&quot; — версия 2,5 (по умолчанию)</p></li>
<li><p>&quot;21&quot; — версия 2,1</p></li>
<li><p>&quot;20&quot; — версия 2,0</p></li>
<li><p>&quot;15&quot; — версия 1,5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Свойства команды</strong></p></td>
<td><p>Указывает значения, которые будут добавлены в строку свойств команды (набора строк), отправляемых на сервер с помощью службы MS Remote. Значение по умолчанию для этой строки — вт_емпти.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Текущая Дфмоде</strong></p></td>
<td><p>Указывает фактический номер версии для объекта <strong>фактов</strong> на сервере. Установите флажок, чтобы проверить, было ли получено требование о версии, заданной в свойстве <strong>дфмоде</strong> . Может принимать одно из следующих допустимых длинных целых значений:</p>
<p></p>
<ul>
<li><p>25 — версия 2,5 (по умолчанию)</p></li>
<li><p>21 — версия 2,1</p></li>
<li><p>20 — версия 2,0</p></li>
<li><p>15 — версия 1,5</p></li>
</ul>
<p></p>
<p>Добавление &quot;дфмоде = 20; &quot; в строку подключения при использовании поставщика <strong>мсремоте</strong> может увеличить производительность сервера при обновлении данных. При использовании этого параметра объект <strong>фактического объекта рдссервер.</strong> DataObject на сервере использует менее ресурсоемкий режим. Однако следующие функции недоступны в этой конфигурации:</p>
<p></p>
<ul>
<li><p>Использование параметризованных запросов.</p></li>
<li><p>Получить сведения о параметрах или столбцах перед вызовом метода <strong>EXECUTE</strong> .</p></li>
<li><p>Установка значения <strong>true</strong>для <strong>обновлений Transact</strong> .</p></li>
<li><p>Получает состояние строки.</p></li>
<li><p>Вызов метода <strong>Resync</strong> .</p></li>
<li><p>Обновление (явно или автоматически) с помощью <strong></strong> свойства Resync.</p></li>
<li><p>Задание свойств <strong>команды</strong> или <strong>набора записей</strong> .</p></li>
<li><p>С помощью <strong>адкмдтабледирект</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Событий</strong></p></td>
<td><p>Указывает имя программы настройки на стороне сервера (или обработчика), которая расширяет функциональные возможности <a href="datafactory-object-rdsserver.md">рдссервер.</a>, и все параметры, используемые обработчиком<em>,</em> разделенные запятыми (&quot;,&quot;). <strong>Строковое</strong> значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Время ожидания в Интернете</strong></p></td>
<td><p>Указывает максимальное время ожидания (в миллисекундах), в течение которого запрос передаются на сервер и с него. (Значение по умолчанию — 5 минут.)</p></td>
</tr>
<tr class="even">
<td><p><strong>Удаленный поставщик</strong></p></td>
<td><p>Указывает имя поставщика данных, который будет использоваться на удаленном сервере.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Удаленный сервер</strong></p></td>
<td><p>Указывает имя сервера и протокол связи, который будет использоваться этим подключением. Это свойство эквивалентно <a href="datacontrol-object-rds.md">RDS. </a>Свойство <a href="server-property-rds.md">сервера</a> объектов DataObject.</p></td>
</tr>
<tr class="even">
<td><p><strong>Обновления Transact</strong></p></td>
<td><p>Если задано значение true, это значение указывает, что когда <a href="updatebatch-method-ado.md">UpdateBatch</a> выполняется на сервере, он будет выполнен внутри транзакции. Значение по умолчанию для этого динамического свойства Boolean равно false.</p></td>
</tr>
</tbody>
</table>


Вы также можете задать динамические свойства для записи, указав их имена в виде ключевых слов в строке подключения. Например, задайте для динамического свойства **время ожидания в Интернете** значение пять секунд, указав следующее:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для свойства **Properties** . Например, получите и распечатайте текущее значение динамического свойства **timeout в Интернете** , а затем задайте новое значение, как показано ниже.

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Замечания

В ADO 2,0 поставщик удаленного взаимодействия OLE DB можно указать только в параметре *ActiveConnection* метода **Open** объекта [Recordset](recordset-object-ado.md) . Начиная с ADO 2,1, поставщик также может быть указан в параметре *ConnectionString* метода **Open** объекта [Connection](connection-object-ado.md) .

Эквивалент объекта **RDS. **Свойство [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) объекта управления DataObject недоступно. Вместо этого используется аргумент *источник* метода **открытия** объекта [Recordset](recordset-object-ado.md) .

Указание "...; Удаленный поставщик = MS Remote;... " создаст сценарий из четырех уровней. Сценарии, находящиеся за пределами трех уровней, не тестировались и не должны быть необходимыми.

## <a name="example"></a>Пример

В этом примере выполняется запрос в таблице **authors** базы данных **pubs** на сервере с именем, *йоурсервер*. Имена удаленного источника данных и удаленного сервера предоставляются в методе [Open](open-method-ado-connection.md) объекта [Connection](connection-object-ado.md) , а запрос SQL задаетСя в методе [Open](open-method-ado-recordset.md) объекта [Recordset](recordset-object-ado.md) . Объект **Recordset** возвращается, редактируется и используется для обновления источника данных.

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

