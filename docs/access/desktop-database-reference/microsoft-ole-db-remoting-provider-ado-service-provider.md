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
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="3de78-102">Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="3de78-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="3de78-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3de78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3de78-104">Поставщик удаленного взаимодействия Microsoft OLE DB позволяет локальному пользователю на клиентском компьютере запускать поставщики данных на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3de78-104">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine.</span></span> <span data-ttu-id="3de78-105">Укажите параметры поставщика данных для удаленного компьютера так же, как если бы вы были локальными пользователями на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3de78-105">Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine.</span></span> <span data-ttu-id="3de78-106">Затем укажите параметры, используемые поставщиком удаленного взаимодействия для доступа к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="3de78-106">Then specify the parameters used by the Remoting Provider to access the remote machine.</span></span> <span data-ttu-id="3de78-107">Полученный результат заключается в том, что вы получите доступ к удаленному компьютеру, как если бы вы были локальным пользователем.</span><span class="sxs-lookup"><span data-stu-id="3de78-107">The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="3de78-108">Ключевое слово Provider</span><span class="sxs-lookup"><span data-stu-id="3de78-108">Provider Keyword</span></span>

<span data-ttu-id="3de78-109">Чтобы вызвать поставщик удаленного взаимодействия OLE DB, укажите следующее ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="3de78-109">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string.</span></span> <span data-ttu-id="3de78-110">(Обратите внимание на пустое пространство в имени поставщика.)</span><span class="sxs-lookup"><span data-stu-id="3de78-110">(Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="3de78-111">Дополнительные ключевые слова</span><span class="sxs-lookup"><span data-stu-id="3de78-111">Additional Keywords</span></span>

<span data-ttu-id="3de78-112">При вызове этого поставщика услуг важны следующие дополнительные ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="3de78-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3de78-113">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="3de78-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="3de78-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3de78-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de78-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-116">Задает имя удаленного источника данных.</span><span class="sxs-lookup"><span data-stu-id="3de78-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="3de78-117">Он передается поставщику удаленного взаимодействия OLE DB для обработки.</span><span class="sxs-lookup"><span data-stu-id="3de78-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="3de78-118">Это ключевое слово эквивалентно <a href="datacontrol-object-rds.md">RDS. </a>Свойство <a href="connect-property-rds.md">Connect</a> объекта DataObject.</span><span class="sxs-lookup"><span data-stu-id="3de78-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="3de78-119">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="3de78-119">Dynamic Properties</span></span>

<span data-ttu-id="3de78-120">При вызове этого поставщика услуг следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3de78-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3de78-121">Имя динамического свойства</span><span class="sxs-lookup"><span data-stu-id="3de78-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="3de78-122">Описание</span><span class="sxs-lookup"><span data-stu-id="3de78-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3de78-123"><strong>Дфмоде</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-124">Указывает режим фактического режима.</span><span class="sxs-lookup"><span data-stu-id="3de78-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="3de78-125">Строка, указывающая желаемую версию объекта <a href="datafactory-object-rdsserver.md">фактического</a> объекта на сервере.</span><span class="sxs-lookup"><span data-stu-id="3de78-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="3de78-126">Задайте это свойство перед открытием подключения, чтобы запросить определенную версию объекта <strong>фактов</strong>.</span><span class="sxs-lookup"><span data-stu-id="3de78-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="3de78-127">Если запрошенная версия недоступна, будет предпринята попытка использовать предыдущую версию.</span><span class="sxs-lookup"><span data-stu-id="3de78-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="3de78-128">Если предыдущая версия отсутствует, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3de78-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="3de78-129">Если <strong>дфмоде</strong> меньше, чем доступная версия, возникнет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3de78-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="3de78-130">Это свойство доступно только для чтения после того, как подключение установлено.</span><span class="sxs-lookup"><span data-stu-id="3de78-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="3de78-131">Может быть одним из следующих допустимых строковых значений:</span><span class="sxs-lookup"><span data-stu-id="3de78-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="3de78-132">&quot;25&quot; — версия 2,5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3de78-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="3de78-133">&quot;21&quot; — версия 2,1</span><span class="sxs-lookup"><span data-stu-id="3de78-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="3de78-134">&quot;20&quot; — версия 2,0</span><span class="sxs-lookup"><span data-stu-id="3de78-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="3de78-135">&quot;15&quot; — версия 1,5</span><span class="sxs-lookup"><span data-stu-id="3de78-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de78-136"><strong>Свойства команды</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-137">Указывает значения, которые будут добавлены в строку свойств команды (набора строк), отправляемых на сервер с помощью службы MS Remote.</span><span class="sxs-lookup"><span data-stu-id="3de78-137">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider.</span></span> <span data-ttu-id="3de78-138">Значение по умолчанию для этой строки — вт_емпти.</span><span class="sxs-lookup"><span data-stu-id="3de78-138">The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de78-139"><strong>Текущая Дфмоде</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-140">Указывает фактический номер версии для объекта <strong>фактов</strong> на сервере.</span><span class="sxs-lookup"><span data-stu-id="3de78-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="3de78-141">Установите флажок, чтобы проверить, было ли получено требование о версии, заданной в свойстве <strong>дфмоде</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de78-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="3de78-142">Может принимать одно из следующих допустимых длинных целых значений:</span><span class="sxs-lookup"><span data-stu-id="3de78-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="3de78-143">25 — версия 2,5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3de78-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="3de78-144">21 — версия 2,1</span><span class="sxs-lookup"><span data-stu-id="3de78-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="3de78-145">20 — версия 2,0</span><span class="sxs-lookup"><span data-stu-id="3de78-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="3de78-146">15 — версия 1,5</span><span class="sxs-lookup"><span data-stu-id="3de78-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="3de78-147">Добавление &quot;дфмоде = 20; &quot; в строку подключения при использовании поставщика <strong>мсремоте</strong> может увеличить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="3de78-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="3de78-148">При использовании этого параметра объект <strong>фактического объекта рдссервер.</strong> DataObject на сервере использует менее ресурсоемкий режим.</span><span class="sxs-lookup"><span data-stu-id="3de78-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="3de78-149">Однако следующие функции недоступны в этой конфигурации:</span><span class="sxs-lookup"><span data-stu-id="3de78-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="3de78-150">Использование параметризованных запросов.</span><span class="sxs-lookup"><span data-stu-id="3de78-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="3de78-151">Получить сведения о параметрах или столбцах перед вызовом метода <strong>EXECUTE</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de78-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="3de78-152">Установка значения <strong>true</strong>для <strong>обновлений Transact</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de78-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="3de78-153">Получает состояние строки.</span><span class="sxs-lookup"><span data-stu-id="3de78-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="3de78-154">Вызов метода <strong>Resync</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de78-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="3de78-155">Обновление (явно или автоматически) с помощью <strong></strong> свойства Resync.</span><span class="sxs-lookup"><span data-stu-id="3de78-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="3de78-156">Задание свойств <strong>команды</strong> или <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3de78-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="3de78-157">С помощью <strong>адкмдтабледирект</strong>.</span><span class="sxs-lookup"><span data-stu-id="3de78-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de78-158"><strong>Событий</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-159">Указывает имя программы настройки на стороне сервера (или обработчика), которая расширяет функциональные возможности <a href="datafactory-object-rdsserver.md">рдссервер.</a>, и все параметры, используемые обработчиком<em>,</em> разделенные запятыми (&quot;,&quot;).</span><span class="sxs-lookup"><span data-stu-id="3de78-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="3de78-160"><strong>Строковое</strong> значение.</span><span class="sxs-lookup"><span data-stu-id="3de78-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de78-161"><strong>Время ожидания в Интернете</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-162">Указывает максимальное время ожидания (в миллисекундах), в течение которого запрос передаются на сервер и с него.</span><span class="sxs-lookup"><span data-stu-id="3de78-162">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</span></span> <span data-ttu-id="3de78-163">(Значение по умолчанию — 5 минут.)</span><span class="sxs-lookup"><span data-stu-id="3de78-163">(The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de78-164"><strong>Удаленный поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-165">Указывает имя поставщика данных, который будет использоваться на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="3de78-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3de78-166"><strong>Удаленный сервер</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-167">Указывает имя сервера и протокол связи, который будет использоваться этим подключением.</span><span class="sxs-lookup"><span data-stu-id="3de78-167">Indicates the server name and communication protocol to be used by this connection.</span></span> <span data-ttu-id="3de78-168">Это свойство эквивалентно <a href="datacontrol-object-rds.md">RDS. </a>Свойство <a href="server-property-rds.md">сервера</a> объектов DataObject.</span><span class="sxs-lookup"><span data-stu-id="3de78-168">This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3de78-169"><strong>Обновления Transact</strong></span><span class="sxs-lookup"><span data-stu-id="3de78-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="3de78-170">Если задано значение true, это значение указывает, что когда <a href="updatebatch-method-ado.md">UpdateBatch</a> выполняется на сервере, он будет выполнен внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="3de78-170">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction.</span></span> <span data-ttu-id="3de78-171">Значение по умолчанию для этого динамического свойства Boolean равно false.</span><span class="sxs-lookup"><span data-stu-id="3de78-171">The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3de78-172">Вы также можете задать динамические свойства для записи, указав их имена в виде ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="3de78-172">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="3de78-173">Например, задайте для динамического свойства **время ожидания в Интернете** значение пять секунд, указав следующее:</span><span class="sxs-lookup"><span data-stu-id="3de78-173">For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="3de78-174">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для свойства **Properties** .</span><span class="sxs-lookup"><span data-stu-id="3de78-174">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property.</span></span> <span data-ttu-id="3de78-175">Например, получите и распечатайте текущее значение динамического свойства **timeout в Интернете** , а затем задайте новое значение, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="3de78-175">For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="3de78-176">Замечания</span><span class="sxs-lookup"><span data-stu-id="3de78-176">Remarks</span></span>

<span data-ttu-id="3de78-177">В ADO 2,0 поставщик удаленного взаимодействия OLE DB можно указать только в параметре *ActiveConnection* метода **Open** объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3de78-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="3de78-178">Начиная с ADO 2,1, поставщик также может быть указан в параметре *ConnectionString* метода **Open** объекта [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3de78-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="3de78-179">Эквивалент объекта \*\*RDS. \*\*Свойство [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) объекта управления DataObject недоступно.</span><span class="sxs-lookup"><span data-stu-id="3de78-179">The equivalent of the **RDS.DataControl** object [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property is not available.</span></span> <span data-ttu-id="3de78-180">Вместо этого используется аргумент *источник* метода **открытия** объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3de78-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="3de78-181">Указание "...; Удаленный поставщик = MS Remote;... " создаст сценарий из четырех уровней. Сценарии, находящиеся за пределами трех уровней, не тестировались и не должны быть необходимыми.</span><span class="sxs-lookup"><span data-stu-id="3de78-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="3de78-182">Пример</span><span class="sxs-lookup"><span data-stu-id="3de78-182">Example</span></span>

<span data-ttu-id="3de78-183">В этом примере выполняется запрос в таблице **authors** базы данных **pubs** на сервере с именем, *йоурсервер*.</span><span class="sxs-lookup"><span data-stu-id="3de78-183">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*.</span></span> <span data-ttu-id="3de78-184">Имена удаленного источника данных и удаленного сервера предоставляются в методе [Open](open-method-ado-connection.md) объекта [Connection](connection-object-ado.md) , а запрос SQL задаетСя в методе [Open](open-method-ado-recordset.md) объекта [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="3de78-184">The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method.</span></span> <span data-ttu-id="3de78-185">Объект **Recordset** возвращается, редактируется и используется для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="3de78-185">A **Recordset** object is returned, edited, and used to update the data source.</span></span>

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

