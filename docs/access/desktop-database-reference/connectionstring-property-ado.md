---
<span data-ttu-id="9ebc3-101"><<<<<<< Название HEAD: TOCTitle свойство ConnectionString (ADO): свойство ConnectionString (ADO) === название: (ADO) и свойство ConnectionString TOCTitle: свойства ConnectionString (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ebc3-101"><<<<<<< HEAD title: ConnectionString Property (ADO) TOCTitle: ConnectionString Property (ADO) ======= title: ConnectionString property (ADO) TOCTitle: ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9ebc3-102">главные ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) ms:contentKeyID: 48547627 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9ebc3-102">master ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) ms:contentKeyID: 48547627 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9ebc3-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="9ebc3-103"><<<<<<< HEAD</span></span>
# <a name="connectionstring-property-ado"></a><span data-ttu-id="9ebc3-104">ConnectionString Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ebc3-104">ConnectionString Property (ADO)</span></span>
=======
# <a name="connectionstring-property-ado"></a><span data-ttu-id="9ebc3-105">Свойство ConnectionString (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ebc3-105">ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9ebc3-106">master</span><span class="sxs-lookup"><span data-stu-id="9ebc3-106">master</span></span>


<span data-ttu-id="9ebc3-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ebc3-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9ebc3-108">Указывает сведения, используемые для установления подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-108">Indicates the information used to establish a connection to a data source.</span></span>

<span data-ttu-id="9ebc3-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="9ebc3-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="9ebc3-110">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9ebc3-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="9ebc3-111">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9ebc3-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="9ebc3-112">master</span><span class="sxs-lookup"><span data-stu-id="9ebc3-112">master</span></span>

<span data-ttu-id="9ebc3-113">Задает или возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-113">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebc3-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ebc3-114">Remarks</span></span>

<span data-ttu-id="9ebc3-115">Свойство **ConnectionString** укажите источник данных, передав строку подробные подключения, содержащую последовательность операторов *= значение* *аргумента* , разделенные точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-115">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="9ebc3-116">ADO поддерживает пять аргументов для свойства **ConnectionString** ; любые другие аргументы передачи непосредственно к поставщику без какой-либо обработки с ADO.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-116">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO.</span></span> <span data-ttu-id="9ebc3-117">Поддерживает ADO аргументы, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-117">The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ebc3-118">Аргумент</span><span class="sxs-lookup"><span data-stu-id="9ebc3-118">Argument</span></span></p></th>
<th><p><span data-ttu-id="9ebc3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="9ebc3-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ebc3-120"><em>Поставщик =</em></span><span class="sxs-lookup"><span data-stu-id="9ebc3-120"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="9ebc3-121">Задает имя поставщика, который используется для подключения.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-121">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebc3-122"><em>Имя файла =</em></span><span class="sxs-lookup"><span data-stu-id="9ebc3-122"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="9ebc3-123">Указывает имя файла от поставщика (например, объект источника постоянных данных), содержащий сведения о подключении к предварительно.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-123">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebc3-124"><em>Удаленный поставщик =</em></span><span class="sxs-lookup"><span data-stu-id="9ebc3-124"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="9ebc3-125">Задает имя поставщика для использования при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-125">Specifies the name of a provider to use when opening a client-side connection.</span></span> <span data-ttu-id="9ebc3-126">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="9ebc3-126">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ebc3-127"><em>Удаленный сервер =</em></span><span class="sxs-lookup"><span data-stu-id="9ebc3-127"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="9ebc3-128">Задает имя пути сервера, который будет использоваться при открытии подключения со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-128">Specifies the path name of the server to use when opening a client-side connection.</span></span> <span data-ttu-id="9ebc3-129">(Служба удаленных данных только.)</span><span class="sxs-lookup"><span data-stu-id="9ebc3-129">(Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ebc3-130"><em>URL-АДРЕС =</em></span><span class="sxs-lookup"><span data-stu-id="9ebc3-130"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="9ebc3-131">Указывает строку подключения, как абсолютный URL-адрес, идентифицирующий ресурс, такой как файл или папку.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-131">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9ebc3-132">После того как использовать свойство **ConnectionString** и откройте объект [подключения](connection-object-ado.md) поставщик может изменить содержимое свойства, например путем сопоставления имен аргументов определенные ADO с их эквивалентами поставщика.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-132">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="9ebc3-133">Свойство **ConnectionString** автоматически наследует значение, используемое для аргумента *ConnectionString* метод [Open](open-method-ado-connection.md) , можно переопределить свойство **ConnectionString** текущей во время вызова метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="9ebc3-133">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="9ebc3-134">Так как *Имя файла* для аргумента вызывает ADO для загрузки соответствующим поставщиком, нельзя передавать аргументы *поставщика* и *Имени файла* .</span><span class="sxs-lookup"><span data-stu-id="9ebc3-134">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="9ebc3-135">Свойство **ConnectionString** — чтение и запись при подключении закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-135">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="9ebc3-136">Дубликаты аргумент **создаваемая** игнорируются.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-136">Duplicates of an argument in the **ConnectionString** property are ignored.</span></span> <span data-ttu-id="9ebc3-137">Последний экземпляр любого аргумента используется.</span><span class="sxs-lookup"><span data-stu-id="9ebc3-137">The last instance of any argument is used.</span></span>

<span data-ttu-id="9ebc3-138">**Службы удаленных данных об использовании** При использовании на объект **подключения** со стороны клиента со значением свойства **ConnectionString** может включать только параметры *Удаленного поставщика* и *Удаленного сервера* .</span><span class="sxs-lookup"><span data-stu-id="9ebc3-138">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

