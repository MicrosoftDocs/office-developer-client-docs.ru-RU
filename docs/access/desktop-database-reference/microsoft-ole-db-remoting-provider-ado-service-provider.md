---
title: Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8e9e6e655198cba28ece0951414af85ec14f26f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878061"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="87b49-102">Поставщик услуг удаленного взаимодействия Microsoft OLE DB (поставщик служб ADO)</span><span class="sxs-lookup"><span data-stu-id="87b49-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="87b49-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87b49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87b49-104">Поставщик удаленного взаимодействия Microsoft OLE DB позволяет локального пользователя на клиентском компьютере для вызова поставщиков данных на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87b49-104">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine.</span></span> <span data-ttu-id="87b49-105">Укажите параметры поставщика данных для удаленного компьютера, как если бы вы были локального пользователя на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87b49-105">Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine.</span></span> <span data-ttu-id="87b49-106">Затем укажите параметры, используемый поставщиком удаленного взаимодействия для доступа к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="87b49-106">Then specify the parameters used by the Remoting Provider to access the remote machine.</span></span> <span data-ttu-id="87b49-107">Итоговый результат — это будет доступ удаленного компьютера, как если бы вы были локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="87b49-107">The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="87b49-108">Ключевое слово поставщика</span><span class="sxs-lookup"><span data-stu-id="87b49-108">Provider Keyword</span></span>

<span data-ttu-id="87b49-109">Чтобы вызвать поставщика OLE DB удаленного взаимодействия, укажите следующие ключевое слово и значение в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="87b49-109">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string.</span></span> <span data-ttu-id="87b49-110">(Примечание свободное место в имени поставщика и имени).</span><span class="sxs-lookup"><span data-stu-id="87b49-110">(Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="87b49-111">Дополнительные ключевые слова</span><span class="sxs-lookup"><span data-stu-id="87b49-111">Additional Keywords</span></span>

<span data-ttu-id="87b49-112">При вызове этого поставщика услуг относятся следующие дополнительные ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="87b49-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87b49-113">Keyword</span><span class="sxs-lookup"><span data-stu-id="87b49-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="87b49-114">Описание</span><span class="sxs-lookup"><span data-stu-id="87b49-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87b49-115"><strong>Источник данных</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-116">Указывает имя к удаленному источнику данных.</span><span class="sxs-lookup"><span data-stu-id="87b49-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="87b49-117">Он передается для поставщика OLE DB удаленного взаимодействия для обработки.</span><span class="sxs-lookup"><span data-stu-id="87b49-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="87b49-118">Ключевое слово this эквивалентно <a href="datacontrol-object-rds.md">RDS. DataControl</a> <a href="connect-property-rds.md">Подключить</a> свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="87b49-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="87b49-119">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="87b49-119">Dynamic Properties</span></span>

<span data-ttu-id="87b49-120">При вызове этого поставщика услуг в семейство сайтов [Свойства](properties-collection-ado.md) объект [подключения](connection-object-ado.md) добавляются следующие динамические свойства.</span><span class="sxs-lookup"><span data-stu-id="87b49-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87b49-121">Имя динамического свойства</span><span class="sxs-lookup"><span data-stu-id="87b49-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="87b49-122">Описание</span><span class="sxs-lookup"><span data-stu-id="87b49-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87b49-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-124">Указывает режим DataFactory.</span><span class="sxs-lookup"><span data-stu-id="87b49-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="87b49-125">Строка, определяющая рекомендуемой версии объекта <a href="datafactory-object-rdsserver.md">DataFactory</a> на сервере.</span><span class="sxs-lookup"><span data-stu-id="87b49-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="87b49-126">Свойства перед открытием подключения к определенной версии <strong>DataFactory</strong>запроса.</span><span class="sxs-lookup"><span data-stu-id="87b49-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="87b49-127">Если запрошенная версия недоступен, будет предпринята попытка использовать предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="87b49-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="87b49-128">Если предыдущая версия не, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="87b49-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="87b49-129">Если <strong>DFMode</strong> меньше, чем доступная версия, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="87b49-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="87b49-130">Это свойство доступно только для чтения после установить соединение.</span><span class="sxs-lookup"><span data-stu-id="87b49-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="87b49-131">Возможны следующие значения: допустимая строка:</span><span class="sxs-lookup"><span data-stu-id="87b49-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="87b49-132">&quot;25&quot; — версии 2.5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87b49-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="87b49-133">&quot;21&quot; — версии 2.1</span><span class="sxs-lookup"><span data-stu-id="87b49-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="87b49-134">&quot;20&quot; — версии 2.0</span><span class="sxs-lookup"><span data-stu-id="87b49-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="87b49-135">&quot;15&quot; — версия 1.5</span><span class="sxs-lookup"><span data-stu-id="87b49-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b49-136"><strong>Свойства команды</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-137">Указывает значения, которые будут добавлены к строке свойства команды (строк), отправленные на сервер с поставщиком удаленного мс.</span><span class="sxs-lookup"><span data-stu-id="87b49-137">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider.</span></span> <span data-ttu-id="87b49-138">Значение по умолчанию для этой строки — vt_empty.</span><span class="sxs-lookup"><span data-stu-id="87b49-138">The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b49-139"><strong>Текущий DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-140">Указывает номер версии фактический <strong>DataFactory</strong> на сервере.</span><span class="sxs-lookup"><span data-stu-id="87b49-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="87b49-141">Проверяет, это свойство, чтобы увидеть, если был учитываться версии, запрошенного в свойстве <strong>DFMode</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b49-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="87b49-142">Может иметь одно из следующих значений длинное целое число:</span><span class="sxs-lookup"><span data-stu-id="87b49-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="87b49-143">25 — версии 2.5 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87b49-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="87b49-144">21 — версии 2.1</span><span class="sxs-lookup"><span data-stu-id="87b49-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="87b49-145">20 — версии 2.0</span><span class="sxs-lookup"><span data-stu-id="87b49-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="87b49-146">15 — версия 1.5</span><span class="sxs-lookup"><span data-stu-id="87b49-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="87b49-147">Добавление &quot;DFMode = 20; &quot; для подключения к строку при использовании поставщика <strong>MSRemote</strong> можно улучшить производительность сервера при обновлении данных.</span><span class="sxs-lookup"><span data-stu-id="87b49-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="87b49-148">С помощью этого параметра, режим менее интенсивно использует объект <strong>RDSServer.DataFactory</strong> на сервере.</span><span class="sxs-lookup"><span data-stu-id="87b49-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="87b49-149">Тем не менее в этой конфигурации недоступны следующие функции:</span><span class="sxs-lookup"><span data-stu-id="87b49-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="87b49-150">Использование запросов с параметрами.</span><span class="sxs-lookup"><span data-stu-id="87b49-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="87b49-151">Получение сведений о параметра или столбца до вызова метода <strong>Execute</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b49-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="87b49-152">Установка <strong>обновлений Transact</strong> <strong>значения True</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b49-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="87b49-153">Начало строки состояния.</span><span class="sxs-lookup"><span data-stu-id="87b49-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="87b49-154">Вызов метода <strong>выполнить повторную синхронизацию</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b49-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="87b49-155">Обновление через свойство <strong>Выполнить повторную синхронизацию обновления</strong> (явно или автоматически).</span><span class="sxs-lookup"><span data-stu-id="87b49-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="87b49-156">Установка свойств <strong>команда</strong> или <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="87b49-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="87b49-157">С помощью <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b49-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b49-158"><strong>Обработчик</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-159">Указывает имя программы настройки на сервере (или обработчик), который расширяет возможности <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>и все параметры, используемые обработчиком<em>,</em> все, разделив их запятыми (&quot;,&quot;).</span><span class="sxs-lookup"><span data-stu-id="87b49-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="87b49-160"><strong>Строковое</strong> значение.</span><span class="sxs-lookup"><span data-stu-id="87b49-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b49-161"><strong>Время ожидания для Интернета</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-162">Указывает максимальное количество миллисекундах время ожидания для передачи запроса на сервер и с него.</span><span class="sxs-lookup"><span data-stu-id="87b49-162">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server.</span></span> <span data-ttu-id="87b49-163">(Значение по умолчанию — 5 минут).</span><span class="sxs-lookup"><span data-stu-id="87b49-163">(The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b49-164"><strong>Удаленный поставщик</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-165">Указывает имя поставщика данных для использования на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="87b49-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87b49-166"><strong>Удаленный сервер</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-167">Указывает имя и связи протоколом использованный для данного подключения.</span><span class="sxs-lookup"><span data-stu-id="87b49-167">Indicates the server name and communication protocol to be used by this connection.</span></span> <span data-ttu-id="87b49-168">Это свойство соответствует параметру <a href="datacontrol-object-rds.md">RDS. DataControl</a> объекта свойства <a href="server-property-rds.md">сервера</a> .</span><span class="sxs-lookup"><span data-stu-id="87b49-168">This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87b49-169"><strong>Transact обновлений</strong></span><span class="sxs-lookup"><span data-stu-id="87b49-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="87b49-170">Если задано значение True, это значение указывает, что при <a href="updatebatch-method-ado.md">UpdateBatch</a> выполняется на сервере, это будет выполнено, внутри транзакции.</span><span class="sxs-lookup"><span data-stu-id="87b49-170">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction.</span></span> <span data-ttu-id="87b49-171">Значение по умолчанию для этого типа Boolean динамические свойства имеет значение False.</span><span class="sxs-lookup"><span data-stu-id="87b49-171">The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="87b49-172">Можно также установить для записи динамические свойства путем указания их имена в качестве ключевых слов в строке подключения.</span><span class="sxs-lookup"><span data-stu-id="87b49-172">You may also set writable dynamic properties by specifying their names as keywords in the connection string.</span></span> <span data-ttu-id="87b49-173">К примеру присвойте свойству динамических **Время ожидания для Интернета** на пять секунд путем указания:</span><span class="sxs-lookup"><span data-stu-id="87b49-173">For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="87b49-174">Можно также задать или получить динамического свойства, указав его имя в качестве индекса в **поле свойства** .</span><span class="sxs-lookup"><span data-stu-id="87b49-174">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property.</span></span> <span data-ttu-id="87b49-175">К примеру получить и печать текущее значение свойства динамических **Время ожидания для Интернета** и задайте новое значение, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="87b49-175">For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="87b49-176">Замечания</span><span class="sxs-lookup"><span data-stu-id="87b49-176">Remarks</span></span>

<span data-ttu-id="87b49-177">В ADO 2.0 поставщик OLE DB об удаленном взаимодействии может быть указан только с помощью параметра *ActiveConnection* метод **Open** объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="87b49-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="87b49-178">Начиная с ADO 2.1, поставщик может также быть указано в параметре *ConnectionString* объекта [подключения к](connection-object-ado.md) методу **Open** .</span><span class="sxs-lookup"><span data-stu-id="87b49-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="87b49-179">Эквивалент **RDS. DataControl** объект свойство [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="87b49-179">The equivalent of the **RDS.DataControl** object [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property is not available.</span></span> <span data-ttu-id="87b49-180">Вместо этого используется метод **Open** *исходный* аргумент объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="87b49-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="87b49-181">Указание «...; Удаленный поставщик = удаленного мс;...» Создать сценарий четыре уровня. Сценарии, чем три уровня не проверялись и не должно быть необходимым.</span><span class="sxs-lookup"><span data-stu-id="87b49-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="87b49-182">Пример</span><span class="sxs-lookup"><span data-stu-id="87b49-182">Example</span></span>

<span data-ttu-id="87b49-183">В этом примере выполняется запрос на таблице **авторов** **pubs** базы данных на сервере с именем, *сервер*.</span><span class="sxs-lookup"><span data-stu-id="87b49-183">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*.</span></span> <span data-ttu-id="87b49-184">Имена удаленному источнику данных и удаленный сервер предоставляются в метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) и SQL-запрос, указанный в метод [Open](open-method-ado-recordset.md) объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="87b49-184">The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method.</span></span> <span data-ttu-id="87b49-185">Объект **набора записей** возвращается, редактировать и используется для обновления источника данных.</span><span class="sxs-lookup"><span data-stu-id="87b49-185">A **Recordset** object is returned, edited, and used to update the data source.</span></span>

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

