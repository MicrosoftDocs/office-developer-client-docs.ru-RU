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
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="70326-102">Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="70326-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="70326-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70326-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70326-104">Поставщик перенастройки Microsoft OLE DB позволяет локальному пользователю на клиентской машине вызывать поставщиков данных на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="70326-104">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine.</span></span> <span data-ttu-id="70326-105">Укажите параметры поставщика данных для удаленной машины так же, как если бы вы были локальным пользователем на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="70326-105">Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine.</span></span> <span data-ttu-id="70326-106">Затем укажите параметры, используемые поставщиком remoting для доступа к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="70326-106">Then specify the parameters used by the Remoting Provider to access the remote machine.</span></span> <span data-ttu-id="70326-107">В результате вы будете получать доступ к удаленному компьютеру так, как если бы вы были локальным пользователем.</span><span class="sxs-lookup"><span data-stu-id="70326-107">The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="70326-108">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="70326-108">Provider Keyword</span></span>

<span data-ttu-id="70326-109">Чтобы вызвать поставщика remoting OLE DB, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="70326-109">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string.</span></span> <span data-ttu-id="70326-110">(Обратите внимание на пустое пространство в имени поставщика.)</span><span class="sxs-lookup"><span data-stu-id="70326-110">(Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="70326-111">Дополнительные ключевые слова</span><span class="sxs-lookup"><span data-stu-id="70326-111">Additional Keywords</span></span>

<span data-ttu-id="70326-112">При вызове этого поставщика услуг релевантны следующие дополнительные ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="70326-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70326-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="70326-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="70326-114">Description</span><span class="sxs-lookup"><span data-stu-id="70326-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70326-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="70326-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-116">Указывает имя удаленного источника данных.</span><span class="sxs-lookup"><span data-stu-id="70326-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="70326-117">Он передается поставщику remoting OLE DB для обработки.</span><span class="sxs-lookup"><span data-stu-id="70326-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="70326-118">Это ключевое слово эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство Подключение объекта DataControl.</a> <a href="connect-property-rds.md"></a></span><span class="sxs-lookup"><span data-stu-id="70326-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="70326-119">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="70326-119">Dynamic Properties</span></span>

<span data-ttu-id="70326-120">При вызове этого поставщика услуг в коллекцию Свойств объекта [Подключения](connection-object-ado.md) добавляются следующие [динамические](properties-collection-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="70326-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70326-121">Динамическое имя свойства</span><span class="sxs-lookup"><span data-stu-id="70326-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="70326-122">Description</span><span class="sxs-lookup"><span data-stu-id="70326-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70326-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="70326-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-124">Указывает режим DataFactory.</span><span class="sxs-lookup"><span data-stu-id="70326-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="70326-125">Строка, которая указывает нужную версию объекта <a href="datafactory-object-rdsserver.md">DataFactory</a> на сервере.</span><span class="sxs-lookup"><span data-stu-id="70326-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="70326-126">Установите это свойство перед открытием подключения, чтобы запросить определенную версию <strong>DataFactory.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="70326-127">Если запрашиваемая версия недоступна, будет предпринята попытка использования предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="70326-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="70326-128">Если предыдущей версии нет, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="70326-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="70326-129">Если <strong>DFMode</strong> меньше доступной версии, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="70326-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="70326-130">Это свойство читается только после подключения.</span><span class="sxs-lookup"><span data-stu-id="70326-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="70326-131">Может быть одним из следующих допустимых значений строки:</span><span class="sxs-lookup"><span data-stu-id="70326-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="70326-132">&quot;25 &quot; — версия 2.5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70326-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="70326-133">&quot;21 &quot; — версия 2.1</span><span class="sxs-lookup"><span data-stu-id="70326-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="70326-134">&quot;20 &quot; — версия 2.0</span><span class="sxs-lookup"><span data-stu-id="70326-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="70326-135">&quot;15 &quot; — версия 1.5</span><span class="sxs-lookup"><span data-stu-id="70326-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70326-136"><strong>Свойства команды</strong></span><span class="sxs-lookup"><span data-stu-id="70326-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-137">Указывает значения, которые будут добавлены в строку свойств команды (rowset), отправленных на сервер поставщиком ms Remote.</span><span class="sxs-lookup"><span data-stu-id="70326-137">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider.</span></span> <span data-ttu-id="70326-138">Значение по умолчанию для этой строки vt_empty.</span><span class="sxs-lookup"><span data-stu-id="70326-138">The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70326-139"><strong>Текущий DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="70326-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-140">Указывает фактическое число версии <strong>DataFactory</strong> на сервере.</span><span class="sxs-lookup"><span data-stu-id="70326-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="70326-141">Ознакомьтесь с этим свойством, чтобы узнать, была ли почтена версии, запрашиваемой в свойстве <strong>DFMode.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="70326-142">Может быть одним из следующих допустимых значений Long integer:</span><span class="sxs-lookup"><span data-stu-id="70326-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="70326-143">25 — версия 2.5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70326-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="70326-144">21 — версия 2.1</span><span class="sxs-lookup"><span data-stu-id="70326-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="70326-145">20 — версия 2.0</span><span class="sxs-lookup"><span data-stu-id="70326-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="70326-146">15 — версия 1.5</span><span class="sxs-lookup"><span data-stu-id="70326-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="70326-147">Добавление DFMode=20; в строку подключения при использовании &quot; &quot; поставщика <strong>MSRemote</strong> может повысить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="70326-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="70326-148">В этом параметре <strong>объект RDSServer.DataFactory</strong> на сервере использует менее ресурсоемкий режим.</span><span class="sxs-lookup"><span data-stu-id="70326-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="70326-149">Однако в этой конфигурации недоступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="70326-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="70326-150">Использование параметризированных запросов.</span><span class="sxs-lookup"><span data-stu-id="70326-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="70326-151">Получение сведений о параметрах или столбцах перед вызовом метода <strong>Execute.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="70326-152">Настройка <strong>обновлений для transact true</strong> <strong>.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="70326-153">Получение статуса строки.</span><span class="sxs-lookup"><span data-stu-id="70326-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="70326-154">Вызов <strong>метода Resync.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="70326-155">Обновление (явно или автоматически) с помощью свойства <strong>Update Resync.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="70326-156">Настройка <strong>свойств Command</strong> или <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="70326-157">Использование <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="70326-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70326-158"><strong>Обработник</strong></span><span class="sxs-lookup"><span data-stu-id="70326-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-159">Указывает имя программы настройки на стороне сервера (или обработчика), которая расширяет функциональность <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>и любые параметры, используемые обработчиком<em>,</em> все разделенные запятой ( &quot; . &quot; ).</span><span class="sxs-lookup"><span data-stu-id="70326-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="70326-160">Значение <strong>String.</strong></span><span class="sxs-lookup"><span data-stu-id="70326-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70326-161"><strong>Время в Интернете</strong></span><span class="sxs-lookup"><span data-stu-id="70326-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-162">Указывает максимальное количество миллисекунд для ожидания запроса на поездку на сервер и с него.</span><span class="sxs-lookup"><span data-stu-id="70326-162">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</span></span> <span data-ttu-id="70326-163">(По умолчанию — 5 минут.)</span><span class="sxs-lookup"><span data-stu-id="70326-163">(The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70326-164"><strong>Удаленный поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="70326-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-165">Указывает имя поставщика данных, который будет использоваться на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="70326-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="70326-166"><strong>Удаленный сервер</strong></span><span class="sxs-lookup"><span data-stu-id="70326-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-167">Указывает имя сервера и протокол связи, которые будут использоваться этим подключением.</span><span class="sxs-lookup"><span data-stu-id="70326-167">Indicates the server name and communication protocol to be used by this connection.</span></span> <span data-ttu-id="70326-168">Это свойство эквивалентно <a href="datacontrol-object-rds.md">RDS. Свойство объекта DataControl</a> <a href="server-property-rds.md">Server.</a></span><span class="sxs-lookup"><span data-stu-id="70326-168">This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="70326-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="70326-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="70326-170">При заданной значении True это значение указывает на то, что при выполнении <a href="updatebatch-method-ado.md">updateBatch</a> на сервере оно будет выполнено внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="70326-170">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction.</span></span> <span data-ttu-id="70326-171">Значение по умолчанию для этого динамического свойства Boolean false.</span><span class="sxs-lookup"><span data-stu-id="70326-171">The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="70326-172">Можно также задать подавные динамические свойства, указав их имена в качестве ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="70326-172">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="70326-173">Например, закажите динамическое свойство **Internet Timeout** до пяти секунд, указав:</span><span class="sxs-lookup"><span data-stu-id="70326-173">For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="70326-174">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса свойства **свойства.**</span><span class="sxs-lookup"><span data-stu-id="70326-174">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property.</span></span> <span data-ttu-id="70326-175">Например, получите и распечатайте текущее значение динамического свойства **Internet Timeout,** а затем установите новое значение, например:</span><span class="sxs-lookup"><span data-stu-id="70326-175">For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="70326-176">Примечания</span><span class="sxs-lookup"><span data-stu-id="70326-176">Remarks</span></span>

<span data-ttu-id="70326-177">В ADO 2.0 поставщик ремоляции OLE DB может быть указан только в параметре *ActiveConnection* метода Open объекта  [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="70326-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="70326-178">Начиная с ADO 2.1, поставщик также может быть указан в *параметре ConnectionString* метода Open объекта [Подключения.](connection-object-ado.md) </span><span class="sxs-lookup"><span data-stu-id="70326-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="70326-179">Эквивалент **RDS. Свойство объекта DataControl** [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) недоступны.</span><span class="sxs-lookup"><span data-stu-id="70326-179">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available.</span></span> <span data-ttu-id="70326-180">Вместо этого используется **аргумент** [Open](recordset-object-ado.md) *method Open.*</span><span class="sxs-lookup"><span data-stu-id="70326-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="70326-181">Указание "...; Удаленный поставщик=MS Remote;..." создаст четырехуровневый сценарий. Сценарии за пределами трех уровней не были протестированы и не должны быть необходимы.</span><span class="sxs-lookup"><span data-stu-id="70326-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="70326-182">Пример</span><span class="sxs-lookup"><span data-stu-id="70326-182">Example</span></span>

<span data-ttu-id="70326-183">В этом примере выполняется запрос  в таблице авторов базы данных пабов на сервере с именем *YourServer*. </span><span class="sxs-lookup"><span data-stu-id="70326-183">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*.</span></span> <span data-ttu-id="70326-184">Имена удаленного источника данных и удаленного сервера [](open-method-ado-connection.md) предоставляются в методе [Open](connection-object-ado.md) объекта Подключения, а запрос [](open-method-ado-recordset.md) SQL указан в методе Open объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="70326-184">The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method.</span></span> <span data-ttu-id="70326-185">Объект **Recordset** возвращается, редактируется и используется для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="70326-185">A **Recordset** object is returned, edited, and used to update the data source.</span></span>

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

