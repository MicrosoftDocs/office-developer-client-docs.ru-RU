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

Поставщик удаленного управления Microsoft OLE DB позволяет локальному пользователю на клиентском компьютере вызывать поставщиков данных на удаленном компьютере. Укажите параметры поставщика данных для удаленного компьютера так же, как если бы вы были локальным пользователем на удаленном компьютере. Затем укажите параметры, используемые поставщиком удаленного управления для доступа к удаленному компьютеру. В результате вы будете получать доступ к удаленному компьютеру, как если бы вы были локальным пользователем.

## <a name="provider-keyword"></a>Ключевое слово поставщика

Чтобы вызвать поставщика OLE DB Remoting Provider, укажите следующее ключевое слово и значение в строке подключения. (Обратите внимание на пустое место в имени поставщика.)

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
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя удаленного источника данных. Он передается поставщику OLE DB Remoting для обработки. Это ключевое слово эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство Connect объекта DataControl.</a> <a href="connect-property-rds.md"></a></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Динамические свойства

При вызове этого поставщика службы в коллекцию свойств объекта [Connection](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Динамическое имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Указывает режим DataFactory. Строка, задав нужную версию объекта <a href="datafactory-object-rdsserver.md">DataFactory</a> на сервере. Установите это свойство перед открытием подключения, чтобы запросить определенную версию <strong>DataFactory.</strong> Если запрашиваемая версия недоступна, будет предпринята попытка использования предыдущей версии. Если предыдущей версии нет, произойдет ошибка. Если <strong>DFMode</strong> меньше доступной версии, произойдет ошибка. После подключения это свойство будет только для чтения. Может иметь одно из следующих допустимого строки:</p>
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
<td><p>Указывает значения, которые будут добавлены в строку свойств команды (rowset), отправленную на сервер удаленным поставщиком MS. Значение по умолчанию для этой строки — vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>Указывает номер фактической версии <strong>DataFactory</strong> на сервере. Проверьте это свойство, чтобы узнать, была ли считана версия, запрашиваемая в свойстве <strong>DFMode.</strong> Может иметь одно из следующих допустимого длинного integer значений:</p>
<p></p>
<ul>
<li><p>25 — версия 2.5 (по умолчанию)</p></li>
<li><p>21 — версия 2.1</p></li>
<li><p>20 — версия 2.0</p></li>
<li><p>15 — версия 1.5</p></li>
</ul>
<p></p>
<p>Добавление DFMode=20; в строку подключения при использовании поставщика &quot; &quot; <strong>MSRemote</strong> может повысить производительность сервера при обновлении данных. С помощью этого параметра объект <strong>RDSServer.DataFactory</strong> на сервере использует менее ресурсоемкий режим. Однако в этой конфигурации недоступны следующие функции:</p>
<p></p>
<ul>
<li><p>Использование параметровизированных запросов.</p></li>
<li><p>Получение сведений о параметре или столбце перед вызовом <strong>метода Execute.</strong></p></li>
<li><p>Установка <strong>для transact-обновлений</strong> <strong>true.</strong></p></li>
<li><p>Получение состояния строки.</p></li>
<li><p>Вызов метода <strong>Resync.</strong></p></li>
<li><p>Обновление (явно или автоматически) с помощью свойства <strong>Update Resync.</strong></p></li>
<li><p>Установка <strong>свойств Command</strong> или <strong>Recordset.</strong></p></li>
<li><p>Использование <strong>adCmdTableDirect.</strong></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Обработник</strong></p></td>
<td><p>Указывает имя программы настройки на стороне сервера (или обработчика), которая расширяет функциональные возможности <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>и любые параметры, используемые обработчиком, разделенные запятой ( ,<em></em> &quot; &quot; ). <strong>Строка.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Указывает максимальное количество миллисекунд для ожидания запроса на доступ к серверу и с него. (Значение по умолчанию — 5 минут.)</p></td>
</tr>
<tr class="even">
<td><p><strong>Удаленный поставщик</strong></p></td>
<td><p>Указывает имя поставщика данных, который будет использоваться на удаленном сервере.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Удаленный сервер</strong></p></td>
<td><p>Указывает имя сервера и протокол связи, которые будут использоваться этим подключением. Это свойство эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство DataControl</a> object <a href="server-property-rds.md">Server.</a></p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>Если установлено значение True, это значение указывает, что при выполнении <a href="updatebatch-method-ado.md">UpdateBatch</a> на сервере оно будет выполняться внутри транзакции. По умолчанию для этого boolean динамического свойства задано значение False.</p></td>
</tr>
</tbody>
</table>


Можно также задать динамические свойства, которые можно переписать, указав их имена в качестве ключевых слов в строке подключения. Например, установите для динамического **свойства Internet Timeout** (Время простоя в Интернете) пять секунд, указав:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса **для свойства Properties.** Например, получите и распечатайте текущее значение динамического свойства **Internet Timeout,** а затем установите новое значение, например:

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Заметки

В ADO 2.0 поставщик OLE DB Remoting может быть указан только в параметре *ActiveConnection* метода [Recordset](recordset-object-ado.md) object **Open.** Начиная с ADO 2.1, поставщик также может быть указан в *параметре ConnectionString* метода [Connection](connection-object-ado.md) object **Open.**

Эквивалент **RDS. Объект DataControl** [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) свойства не доступен. Вместо этого используется  аргумент метода Open объекта [Recordset.](recordset-object-ado.md) 

Указание "...; Удаленный поставщик=MS Remote;..." создает четырехуровневый сценарий. Сценарии, которые выходят за три уровня, не были протестированы и не нужны.

## <a name="example"></a>Пример

В этом примере выполняется запрос к таблице авторов базы данных **pubs** на сервере с именем *YourServer.*  Имена удаленного источника данных и удаленного сервера предоставляются в методе [Connection](connection-object-ado.md) object [Open,](open-method-ado-connection.md) а запрос [](open-method-ado-recordset.md) SQL указывается в методе Open объекта [Recordset.](recordset-object-ado.md) Объект **Recordset** возвращается, редактируется и используется для обновления источника данных.

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

