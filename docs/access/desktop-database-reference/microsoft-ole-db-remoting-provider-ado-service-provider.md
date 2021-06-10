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

Поставщик перенастройки Microsoft OLE DB позволяет локальному пользователю на клиентской машине вызывать поставщиков данных на удаленном компьютере. Укажите параметры поставщика данных для удаленной машины так же, как если бы вы были локальным пользователем на удаленном компьютере. Затем укажите параметры, используемые поставщиком remoting для доступа к удаленному компьютеру. В результате вы будете получать доступ к удаленному компьютеру так, как если бы вы были локальным пользователем.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать поставщика remoting OLE DB, укажите следующее ключевое слово и значение в строке подключения. (Обратите внимание на пустое пространство в имени поставщика.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Дополнительные ключевые слова

При вызове этого поставщика услуг релевантны следующие дополнительные ключевые слова.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя удаленного источника данных. Он передается поставщику remoting OLE DB для обработки. Это ключевое слово эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство Подключение объекта DataControl.</a> <a href="connect-property-rds.md"></a></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Dynamic Properties

При вызове этого поставщика услуг в коллекцию Свойств объекта [Подключения](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Динамическое имя свойства</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Указывает режим DataFactory. Строка, которая указывает нужную версию объекта <a href="datafactory-object-rdsserver.md">DataFactory</a> на сервере. Установите это свойство перед открытием подключения, чтобы запросить определенную версию <strong>DataFactory.</strong> Если запрашиваемая версия недоступна, будет предпринята попытка использования предыдущей версии. Если предыдущей версии нет, произойдет ошибка. Если <strong>DFMode</strong> меньше доступной версии, произойдет ошибка. Это свойство читается только после подключения. Может быть одним из следующих допустимых значений строки:</p>
<p></p>
<ul>
<li><p>&quot;25 &quot; — версия 2.5 (по умолчанию)</p></li>
<li><p>&quot;21 &quot; — версия 2.1</p></li>
<li><p>&quot;20 &quot; — версия 2.0</p></li>
<li><p>&quot;15 &quot; — версия 1.5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Свойства команды</strong></p></td>
<td><p>Указывает значения, которые будут добавлены в строку свойств команды (rowset), отправленных на сервер поставщиком ms Remote. Значение по умолчанию для этой строки vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Текущий DFMode</strong></p></td>
<td><p>Указывает фактическое число версии <strong>DataFactory</strong> на сервере. Ознакомьтесь с этим свойством, чтобы узнать, была ли почтена версии, запрашиваемой в свойстве <strong>DFMode.</strong> Может быть одним из следующих допустимых значений Long integer:</p>
<p></p>
<ul>
<li><p>25 — версия 2.5 (по умолчанию)</p></li>
<li><p>21 — версия 2.1</p></li>
<li><p>20 — версия 2.0</p></li>
<li><p>15 — версия 1.5</p></li>
</ul>
<p></p>
<p>Добавление DFMode=20; в строку подключения при использовании &quot; &quot; поставщика <strong>MSRemote</strong> может повысить производительность сервера при обновлении данных. В этом параметре <strong>объект RDSServer.DataFactory</strong> на сервере использует менее ресурсоемкий режим. Однако в этой конфигурации недоступны следующие функции:</p>
<p></p>
<ul>
<li><p>Использование параметризированных запросов.</p></li>
<li><p>Получение сведений о параметрах или столбцах перед вызовом метода <strong>Execute.</strong></p></li>
<li><p>Настройка <strong>обновлений для transact true</strong> <strong>.</strong></p></li>
<li><p>Получение статуса строки.</p></li>
<li><p>Вызов <strong>метода Resync.</strong></p></li>
<li><p>Обновление (явно или автоматически) с помощью свойства <strong>Update Resync.</strong></p></li>
<li><p>Настройка <strong>свойств Command</strong> или <strong>Recordset.</strong></p></li>
<li><p>Использование <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Обработник</strong></p></td>
<td><p>Указывает имя программы настройки на стороне сервера (или обработчика), которая расширяет функциональность <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>и любые параметры, используемые обработчиком<em>,</em> все разделенные запятой ( &quot; . &quot; ). Значение <strong>String.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Время в Интернете</strong></p></td>
<td><p>Указывает максимальное количество миллисекунд для ожидания запроса на поездку на сервер и с него. (По умолчанию — 5 минут.)</p></td>
</tr>
<tr class="even">
<td><p><strong>Удаленный поставщик</strong></p></td>
<td><p>Указывает имя поставщика данных, который будет использоваться на удаленном сервере.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Удаленный сервер</strong></p></td>
<td><p>Указывает имя сервера и протокол связи, которые будут использоваться этим подключением. Это свойство эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство объекта DataControl</a> <a href="server-property-rds.md">Server.</a></p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>При заданной значении True это значение указывает на то, что при выполнении <a href="updatebatch-method-ado.md">updateBatch</a> на сервере оно будет выполнено внутри транзакции. Значение по умолчанию для этого динамического свойства Boolean false.</p></td>
</tr>
</tbody>
</table>


Можно также задать подавные динамические свойства, указав их имена в качестве ключевых слов в строке подключения. Например, закажите динамическое свойство **Internet Timeout** до пяти секунд, указав:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса свойства **свойства.** Например, получите и распечатайте текущее значение динамического свойства **Internet Timeout,** а затем установите новое значение, например:

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Примечания

В ADO 2.0 поставщик ремоляции OLE DB может быть указан только в параметре *ActiveConnection* метода Open объекта  [Recordset.](recordset-object-ado.md) Начиная с ADO 2.1, поставщик также может быть указан в *параметре ConnectionString* метода Open объекта [Подключения.](connection-object-ado.md) 

Эквивалент **RDS. Свойство объекта DataControl** [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) недоступны. Вместо этого используется **аргумент** [Open](recordset-object-ado.md) *method Open.*

Указание "...; Удаленный поставщик=MS Remote;..." создаст четырехуровневый сценарий. Сценарии за пределами трех уровней не были протестированы и не должны быть необходимы.

## <a name="example"></a>Пример

В этом примере выполняется запрос  в таблице авторов базы данных пабов на сервере с именем *YourServer*.  Имена удаленного источника данных и удаленного сервера [](open-method-ado-connection.md) предоставляются в методе [Open](connection-object-ado.md) объекта Подключения, а запрос [](open-method-ado-recordset.md) SQL указан в методе Open объекта [Recordset.](recordset-object-ado.md) Объект **Recordset** возвращается, редактируется и используется для обновления источника данных.

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

